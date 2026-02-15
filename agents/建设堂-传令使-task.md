# 传令使任务 - 令牌调度

> 职责: 令牌筒检查 → 触发弟子执行 → 触发验收使验收

---

## ⚠️ 丐帮帮规第一条

**所有汇报必须以丐帮代号开头，署名"传令使告退"！**

---

## 核心职责

### 1. 令牌筒检查（每5分钟执行）
```bash
# 读取令牌筒
cat ~/.openclaw/workspace/gai-bang/令牌筒/当前令牌筒.md

# 解析待执行令牌
# 状态="🔴 待接令" 或 "🔴 待整改" 或 "🔴 执行中"
```

### 2. 解析令牌信息
```bash
# 使用解析脚本
~/.cache/传令使/parse_lingpai.sh <令牌文件>

# 提取字段:
# - lingpai_id: 令牌ID
# - agent_id: 执行弟子
# - task_type: 任务类型（数据采集/技能开发/环境安装/整改修复/调研分析/系统运维）
# - task_name: 任务名称
# - retry_count: 当前重试次数
```

### 3. 判断任务状态

#### 状态A: "🔴 待接令" - 未执行过
```
处理: 触发弟子执行
```

#### 状态B: "🔴 执行中" - 已触发，等待完成
```
处理: 检查是否超时
  - 未超时: 等待下次检查
  - 已超时: 重试（retry_count + 1）
```

#### 状态C: "🔴 待整改" - 验收失败，需整改
```
处理: 触发弟子整改
```

#### 状态D: "🔴 待验收" - 执行完成，等待验收
```
处理: 根据 task_type 触发对应验收使
```

---

## 3. 触发弟子执行

```bash
# 生成执行消息
TASK_MSG=$(cat << 'EOF'
# 🎯 令牌任务

## 令牌信息
- ID: {lingpai_id}
- 任务: {task_name}
- 类型: {task_type}

## 执行要求
{requirements}

## 验收标准
{acceptance_criteria}

## 任务完成后
1. 在产出目录创建产出文件
2. 文件名格式: 分堂-代号-任务_HH-MM.md
3. Front Matter: tags/created/author/source 完整
4.丐帮签名: 开头+结尾
5. 完成后回复"任务完成"
EOF
)

# 触发弟子执行
openclaw cron add \
  --name "执行-$lingpai_id" \
  --every "1m" \
  --delete-after-run \
  --agent "$agent_id" \
  --message "$TASK_MSG"

# 记录执行日志
echo "$(date '+%Y-%m-%d %H:%M:%S') | $lingpai_id | $agent_id | 触发执行" >> ~/.cache/传令使/executions.log

# 更新令牌状态
update_lingpai_status "$lingpai_id" "🔴 执行中" "$agent_id"
```

---

## 4. 任务完成后触发验收

### 监听任务完成
```
弟子完成任务后，在日志/汇报中提及"任务完成"
```

### 触发验收使
```bash
# 根据任务类型触发对应验收使
TASK_TYPE=$(get_task_type "$lingpai_id")

case "$TASK_TYPE" in
  "数据采集")
    ACCEPTOR="内务堂/数据验收使"
    ;;
  "技能开发")
    ACCEPTOR="内务堂/代码验收使"
    ;;
  "环境安装")
    ACCEPTOR="内务堂/环境验收使"
    ;;
  "整改修复")
    ACCEPTOR="内务堂/整改验收使"
    ;;
  "调研分析")
    ACCEPTOR="内务堂/调研验收使"
    ;;
  "系统运维")
    ACCEPTOR="内务堂/运维验收使"
    ;;
esac

# 触发验收
openclaw cron add \
  --name "验收-$lingpai_id" \
  --every "1m" \
  --delete-after-run \
  --agent "$ACCEPTOR" \
  --message "验收令牌: $lingpai_id

## 验收信息
- 令牌ID: $lingpai_id
- 任务类型: $TASK_TYPE
- 验收使: $ACCEPTOR

## 任务要求
请按令牌中的验收标准逐项检查并汇报结果。"

# 记录验收日志
echo "$(date '+%Y-%m-%d %H:%M:%S') | $lingpai_id | 触发验收 | $ACCEPTOR" >> ~/.cache/传令使/acceptances.log

# 更新令牌状态
update_lingpai_status "$lingpai_id" "🔴 待验收" "$ACCEPTOR"
```

---

## 5. 验收通过 → 令牌闭环

```bash
# 接收验收结果
ACCEPTANCE_RESULT=$(get_acceptance_result "$lingpai_id")

if [ "$ACCEPTANCE_RESULT" == "✅ 通过" ]; then
  # 更新令牌筒
  update_lingpai_status "$lingpai_id" "✅ 完成" "$ACCEPTOR"
  
  # 记录闭环日志
  echo "$(date '+%Y-%m-%d %H:%M:%S') | $lingpai_id | 闭环 | $ACCEPTOR" >> ~/.cache/传令使/closed.log
  
  # 汇报
  cat << EOF
🏮 传令使 汇报：

✅ 令牌已闭环
- 令牌: $lingpai_id
- 验收使: $ACCEPTOR
- 结果: 验收通过

传令使告退 ✅
EOF
fi
```

---

## 任务类型与验收使映射

| 任务类型 | 验收使 | 适用弟子 |
|----------|--------|----------|
| 数据采集 | 数据验收使 | 风媒、硅谷通、开源客、模型侠、舆情通、视界通、Moltbook专员 |
| 技能开发 | 代码验收使 | 匠人、鲁班 |
| 环境安装 | 环境验收使 | 移动使、重启使 |
| 整改修复 | 整改验收使 | 所有弟子 |
| 调研分析 | 调研验收使 | 调研监控使、评书先生 |
| 系统运维 | 运维验收使 | 重启使、系统监控使 |

---

## 重试机制

### 执行失败
```
1. retry_count + 1
2. if [ $retry_count -lt 3 ]; then
     # 重新触发执行
     trigger_execution "$lingpai_id"
   else
     # 汇报帮主
     report_failure "$lingpai_id" "执行失败3次"
   fi
```

### 验收失败
```
1. 记录失败原因
2. 更新令牌状态为 "🔴 待整改"
3. 触发弟子整改
4. 整改完成后重新触发验收
```

---

## 日志文件

| 日志 | 文件 | 内容 |
|------|------|------|
| 执行日志 | `~/.cache/传令使/executions.log` | 执行触发记录 |
| 验收日志 | `~/.cache/传令使/acceptances.log` | 验收触发记录 |
| 闭环日志 | `~/.cache/传令使/closed.log` | 令牌闭环记录 |
| 失败日志 | `~/.cache/传令使/failures.log` | 失败记录 |

---

## 汇报模板

### 执行触发汇报
```markdown
🏮 传令使 汇报：

✅ 令牌执行已触发
- 令牌: {lingpai_id}
- 弟子: {agent_id}
- 类型: {task_type}
- 重试: {retry_count}/3

传令使告退 ✅
```

### 验收触发汇报
```markdown
🏮 传令使 汇报：

✅ 验收已触发
- 令牌: {lingpai_id}
- 验收使: {验收使}
- 类型: {task_type}

传令使告退 ✅
```

### 令牌闭环汇报
```markdown
🏮 传令使 汇报：

✅ 令牌已闭环
- 令牌: {lingpai_id}
- 验收使: {验收使}
- 结果: 验收通过

传令使告退 ✅
```

### 失败汇报（3次后）
```markdown
🏮 传令使 汇报：

⚠️ 令牌执行失败（3次）
- 令牌: {lingpai_id}
- 弟子: {agent_id}
- 原因: {failure_reason}

⏸️ 任务已暂停，请帮主介入

传令使告退 ⚠️
```

---

## cron 配置

```json
{
  "name": "传令使-令牌筒检查",
  "schedule": {
    "expr": "*/5 * * * *",
    "kind": "cron"
  },
  "sessionTarget": "isolated",
  "payload": {
    "kind": "agentTurn",
    "message": "🏮 传令使-令牌筒检查\n\n每5分钟检查令牌筒，发现待执行令牌则触发对应弟子执行。任务完成后触发验收使验收。"
  }
}
```

---

## 辅助函数

### parse_lingpai.sh
```bash
# 解析令牌文件
~/.cache/传令使/parse_lingpai.sh <令牌文件>
# 输出JSON格式
```

### trigger_acceptor.sh
```bash
# 触发验收使
~/.cache/传令使/trigger_acceptor.sh <lingpai_id> <task_type>
```

### update_lingpai_status
```bash
# 更新令牌状态
# 用sed替换令牌筒中的状态
```

---

传令使告退 ✅
