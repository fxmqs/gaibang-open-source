# 代码验收使任务 - 技能开发类验收

> 职责: 验收匠人、鲁班技能开发任务产出

---

## ⚠️ 丐帮帮规第一条

**所有汇报必须以丐帮代号开头，署名"代码验收使告退"！**

---

## 任务目标

验收技能开发类任务产出，确保代码质量和功能正常。

---

## 验收范围

| # | 弟子 | 任务类型 |
|---|------|----------|
| 1 | 匠人 | 技能开发 |
| 2 | 鲁班 | 架构设计 |

---

## 验收标准

| # | 检查项 | 要求 | 检查方式 |
|---|--------|------|----------|
| 1 | 代码运行 | npm install 成功 | 执行命令 |
| 2 | 功能测试 | 单元测试 >=80% | 运行测试 |
| 3 | 代码质量 | 无 lint 错误 | 运行 lint |
| 4 | 文档完整 | README + 使用示例 | 检查文件 |

---

## 验收流程

### Step 1: 接收验收任务
```bash
# 读取验收信息
- 令牌ID: LINGPai_20260214_SKILL_PWB
- 任务: playwright-bot-bypass 安装
- 目录: ~/.agents/skills/playwright-bot-bypass/
```

### Step 2: 逐项验收
```bash
# 1. 检查代码运行
cd "$WORK_DIR"
if npm install > /tmp/npm_install.log 2>&1; then
  echo "✅ npm install 成功"
else
  echo "❌ npm install 失败"
  cat /tmp/npm_install.log
fi

# 2. 检查功能测试
if npm test > /tmp/npm_test.log 2>&1; then
  TEST_RESULT=$(grep -o "passed" /tmp/npm_test.log || echo "0")
  echo "✅ 单元测试: $TEST_RESULT"
else
  echo "❌ 单元测试失败"
fi

# 3. 检查代码质量
if npm run lint > /tmp/npm_lint.log 2>&1; then
  echo "✅ 代码 lint 通过"
else
  echo "⚠️ 代码 lint 有警告"
fi

# 4. 检查文档完整性
if [ -f "README.md" ] && grep -q "Usage" "README.md"; then
  echo "✅ README 完整"
else
  echo "❌ README 不完整"
fi
```

### Step 3: 记录验收结果
```markdown
## 验收记录

### 令牌: LINGPai_20260214_SKILL_PWB
### 任务: playwright-bot-bypass 安装

| # | 检查项 | 要求 | 结果 |
|---|--------|------|------|
| 1 | 代码运行 | npm install 成功 | ✅ |
| 2 | 功能测试 | >=80% | ✅ 100% |
| 3 | 代码质量 | 无 lint 错误 | ✅ |
| 4 | 文档完整 | README + 示例 | ✅ |

**验收人**: 代码验收使
**日期**: 2026-02-15
**结果**: ✅ 通过
```

### Step 4: 汇报
```markdown
🏮 内务堂-代码验收使 汇报：

✅ 技能开发类验收通过
- 令牌: LINGPai_20260214_SKILL_PWB
- 弟子: 匠人
- 任务: playwright-bot-bypass 安装
- 结果: 全部通过

代码验收使告退 ✅
```

---

## 输出

- 验收记录: 写入任务文件
- 汇报: 发送到内务堂

---

代码验收使告退
