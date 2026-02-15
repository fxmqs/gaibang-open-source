# 重启使任务 - Gateway 重启与监控

## ⚠️ 丐帮帮规第一条

## 📁 输出目录规范 ✅ 墨刑审核项

> 见《丐帮目录结构规范》: `gai-bang/内务堂/丐帮目录结构规范.md`

### 目录结构

```
Inbox/YYYY-MM-DD/分堂/弟子代号/
└── 分堂-代号-任务_HH-MM.md
```

### Front Matter

```yaml
---
tags: #[标签]
created: YYYY-MM-DDTHH:MM:SS+08:00
author: 分堂-代号
source: 数据来源
---
```


**所有汇报必须以丐帮代号开头，署名"某某告退"！**
> 违反此帮规 = 不合格产出

---

## 任务目标

## 📁 输出目录规范 ✅ 墨刑审核项

> 见《丐帮目录结构规范》: `gai-bang/内务堂/丐帮目录结构规范.md`

### 目录结构

```
Inbox/YYYY-MM-DD/分堂/弟子代号/
└── 分堂-代号-任务_HH-MM.md
```

### Front Matter

```yaml
---
tags: #[标签]
created: YYYY-MM-DDTHH:MM:SS+08:00
author: 分堂-代号
source: 数据来源
---
```


监控 Gateway 重启状态，执行重启操作，验证重启结果。

## 文件路径

## 📁 输出目录规范 ✅ 墨刑审核项

> 见《丐帮目录结构规范》: `gai-bang/内务堂/丐帮目录结构规范.md`

### 目录结构

```
Inbox/YYYY-MM-DD/分堂/弟子代号/
└── 分堂-代号-任务_HH-MM.md
```

### Front Matter

```yaml
---
tags: #[标签]
created: YYYY-MM-DDTHH:MM:SS+08:00
author: 分堂-代号
source: 数据来源
---
```


### 核心文件

| 文件 | 路径 | 说明 |
|------|------|------|
| **重启标志** | `/Users/long.zhu/.openclaw/gateway_restart_flag.txt` | 0=需要重启，1=不需要 |
| **重启日志** | `/Users/long.zhu/.openclaw/gateway_restart.log` | 重启过程记录 |
| **Stdout** | `/Users/long.zhu/.openclaw/gateway_monitor.stdout.log` | 脚本输出 |
| **Stderr** | `/Users/long.zhu/.openclaw/gateway_monitor.stderr.log` | 错误信息 |

---

## 检查流程

## 📁 输出目录规范 ✅ 墨刑审核项

> 见《丐帮目录结构规范》: `gai-bang/内务堂/丐帮目录结构规范.md`

### 目录结构

```
Inbox/YYYY-MM-DD/分堂/弟子代号/
└── 分堂-代号-任务_HH-MM.md
```

### Front Matter

```yaml
---
tags: #[标签]
created: YYYY-MM-DDTHH:MM:SS+08:00
author: 分堂-代号
source: 数据来源
---
```


### 第一步：检查重启标志

```bash
cat /Users/long.zhu/.openclaw/gateway_restart_flag.txt
```

| 值 | 含义 | 操作 |
|----|------|------|
| 0 | 需要重启 | 执行重启操作 |
| 1 | 不需要重启 | 检查日志状态 |

### 第二步：查看重启日志

```bash
cat /Users/long.zhu/.openclaw/gateway_restart.log
```

**日志格式**:

成功:
```
[2026-02-12 21:58:45] 检测到重启标志，开始重启 gateway...
[2026-02-12 21:58:45] Gateway 重启成功
[2026-02-12 21:58:45] 已重置标志为 1
```

失败:
```
[2026-02-12 xx:xx:xx] 检测到重启标志，开始重启 gateway...
[2026-02-12 xx:xx:xx] Gateway 重启失败
```

### 第三步：查看监控日志（可选）

```bash
# Stdout
cat /Users/long.zhu/.openclaw/gateway_monitor.stdout.log

# Stderr
cat /Users/long.zhu/.openclaw/gateway_monitor.stderr.log
```

---

## 执行方式

## 📁 输出目录规范 ✅ 墨刑审核项

> 见《丐帮目录结构规范》: `gai-bang/内务堂/丐帮目录结构规范.md`

### 目录结构

```
Inbox/YYYY-MM-DD/分堂/弟子代号/
└── 分堂-代号-任务_HH-MM.md
```

### Front Matter

```yaml
---
tags: #[标签]
created: YYYY-MM-DDTHH:MM:SS+08:00
author: 分堂-代号
source: 数据来源
---
```


### 方式一：自动监控

监控脚本每分钟自动检查 flag 文件，检测到 0 时自动重启。

### 方式二：手动执行

```bash
# 标记需要重启
echo '0' > /Users/long.zhu/.openclaw/gateway_restart_flag.txt

# 或者手动重启
openclaw gateway restart
```

### 方式三：重启使检查

**手动调用重启使检查状态**

1. 检查 flag 值
2. 查看重启日志
3. 验证重启结果
4. 输出状态报告

---

## 输出报告格式

## 📁 输出目录规范 ✅ 墨刑审核项

> 见《丐帮目录结构规范》: `gai-bang/内务堂/丐帮目录结构规范.md`

### 目录结构

```
Inbox/YYYY-MM-DD/分堂/弟子代号/
└── 分堂-代号-任务_HH-MM.md
```

### Front Matter

```yaml
---
tags: #[标签]
created: YYYY-MM-DDTHH:MM:SS+08:00
author: 分堂-代号
source: 数据来源
---
```


### 状态报告

```markdown
🏮 建设堂-重启使 汇报：

## Gateway 状态检查

## 📁 输出目录规范 ✅ 墨刑审核项

> 见《丐帮目录结构规范》: `gai-bang/内务堂/丐帮目录结构规范.md`

### 目录结构

```
Inbox/YYYY-MM-DD/分堂/弟子代号/
└── 分堂-代号-任务_HH-MM.md
```

### Front Matter

```yaml
---
tags: #[标签]
created: YYYY-MM-DDTHH:MM:SS+08:00
author: 分堂-代号
source: 数据来源
---
```


### 1. 重启标志

| 标志值 | 含义 | 时间 |
|--------|------|------|
| 1 | 不需要重启 | 2026-02-12 22:03:05 |

### 2. 重启日志

| 时间 | 状态 | 说明 |
|------|------|------|
| 2026-02-12 21:58:45 | 成功 | Gateway 重启成功 |
| 2026-02-12 21:58:45 | 已重置 | 标志已设为 1 |

### 3. 最近日志

```
[2026-02-12 21:58:45] 检测到重启标志，开始重启 gateway...
[2026-02-12 21:58:45] Gateway 重启成功
[2026-02-12 21:58:45] 已重置标志为 1
```

### 4. 结论

✅ Gateway 正常运行
✅ 重启监控正常

---

重启使告退 ✅
```

---

## 故障排查

## 📁 输出目录规范 ✅ 墨刑审核项

> 见《丐帮目录结构规范》: `gai-bang/内务堂/丐帮目录结构规范.md`

### 目录结构

```
Inbox/YYYY-MM-DD/分堂/弟子代号/
└── 分堂-代号-任务_HH-MM.md
```

### Front Matter

```yaml
---
tags: #[标签]
created: YYYY-MM-DDTHH:MM:SS+08:00
author: 分堂-代号
source: 数据来源
---
```


### 常见问题

| 问题 | 可能原因 | 解决方案 |
|------|----------|----------|
| 重启失败 | Gateway 进程卡住 | 手动执行 `openclaw gateway restart` |
| 日志不更新 | 监控脚本未运行 | 检查 cron 任务 |
| 标志不变 | 重启后未设置 | 确认监控脚本逻辑 |

### 日志查看技巧

```bash
# 查看最近 10 行日志
tail -n 10 /Users/long.zhu/.openclaw/gateway_restart.log

# 实时监控日志
tail -f /Users/long.zhu/.openclaw/gateway_restart.log

# 搜索错误
grep -i "失败" /Users/long.zhu/.openclaw/gateway_restart.log
```

---

## 汇报

## 📁 输出目录规范 ✅ 墨刑审核项

> 见《丐帮目录结构规范》: `gai-bang/内务堂/丐帮目录结构规范.md`

### 目录结构

```
Inbox/YYYY-MM-DD/分堂/弟子代号/
└── 分堂-代号-任务_HH-MM.md
```

### Front Matter

```yaml
---
tags: #[标签]
created: YYYY-MM-DDTHH:MM:SS+08:00
author: 分堂-代号
source: 数据来源
---
```


完成后汇报（使用 message 工具发送到当前聊天）：
```markdown
🏮 建设堂-重启使 汇报：

## Gateway 状态检查

## 📁 输出目录规范 ✅ 墨刑审核项

> 见《丐帮目录结构规范》: `gai-bang/内务堂/丐帮目录结构规范.md`

### 目录结构

```
Inbox/YYYY-MM-DD/分堂/弟子代号/
└── 分堂-代号-任务_HH-MM.md
```

### Front Matter

```yaml
---
tags: #[标签]
created: YYYY-MM-DDTHH:MM:SS+08:00
author: 分堂-代号
source: 数据来源
---
```


### 1. 重启标志
- 当前值: [值]
- 含义: [说明]
- 检查时间: [时间]

### 2. 重启日志
- 总行数: [数量]
- 最后状态: [成功/失败/无记录]
- 最后日志: [最后一条日志]

### 3. 结论
✅ Gateway 状态: [正常/异常]
✅ 重启监控: [正常/异常]

重启使告退 ✅
```

---

**重要**：
- ✅ 丐帮代号开头
- ✅ 署名"重启使告退"
- ✅ 用表格呈现数据
