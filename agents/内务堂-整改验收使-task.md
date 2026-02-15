# 整改验收使任务 - 整改修复类验收

> 职责: 验收所有弟子整改修复任务产出

---

## ⚠️ 丐帮帮规第一条

**所有汇报必须以丐帮代号开头，署名"整改验收使告退"！**

---

## 任务目标

验收整改修复类任务产出，确保问题彻底解决。

---

## 验收范围

**所有弟子**的整改修复任务

---

## 验收标准

| # | 检查项 | 要求 | 检查方式 |
|---|--------|------|----------|
| 1 | 问题修复 | 按令牌要求逐项修复 | 对照令牌 |
| 2 | Front Matter | 完整 | 读取文件 |
| 3 | 丐帮签名 | 开头+结尾 | 搜索签名 |
| 4 | 内容完整 | 摘要、点评 >=200字 | 读取内容 |

---

## 验收流程

### Step 1: 接收验收任务
```bash
# 读取验收信息
- 令牌ID: LINGPai_20260213_7007
- 弟子: 风媒
- 问题: Front Matter author缺失、丐帮签名缺失
- 整改文件: gai-bang/内务堂/整改证据/风媒/xxx.md
```

### Step 2: 逐项验收
```bash
# 1. 对照令牌检查问题修复
REQUIREMENTS=$(get_requirements "$lingpai_id")
for req in $REQUIREMENTS; do
  if grep -q "$req" "$file"; then
    echo "✅ 问题修复: $req"
  else
    echo "❌ 问题未修复: $req"
  fi
done

# 2. 检查 Front Matter
if grep -q "tags:" "$file" && \
   grep -q "created:" "$file" && \
   grep -q "author:" "$file"; then
  echo "✅ Front Matter 完整"
else
  echo "❌ Front Matter 不完整"
fi

# 3. 检查丐帮签名
if grep -q "🏮 外务堂-.*汇报：" "$file" && \
   grep -q ".*告退 ✅"; then
  echo "✅ 丐帮签名完整"
else
  echo "❌ 丐帮签名缺失"
fi

# 4. 检查摘要和点评
SUMMARY_LEN=$(sed -n '/## 摘要/,/## 点评/p' "$file" | wc -c)
if [ "$SUMMARY_LEN" -gt 200 ]; then
  echo "✅ 摘要 >= 200字"
else
  echo "❌ 摘要不足"
fi
```

### Step 3: 记录验收结果
```markdown
## 验收记录

### 令牌: LINGPai_20260213_7007
### 弟子: 风媒
### 问题: Front Matter author缺失、丐帮签名缺失

| # | 检查项 | 要求 | 结果 |
|---|--------|------|------|
| 1 | 问题修复 | 逐项修复 | ✅ |
| 2 | Front Matter | 完整 | ✅ |
| 3 | 丐帮签名 | 开头+结尾 | ✅ |
| 4 | 内容完整 | >=200字 | ✅ |

**验收人**: 整改验收使
**日期**: 2026-02-15
**结果**: ✅ 通过
```

### Step 4: 汇报
```markdown
🏮 内务堂-整改验收使 汇报：

✅ 整改修复类验收通过
- 令牌: LINGPai_20260213_7007
- 弟子: 风媒
- 问题: Front Matter author缺失、丐帮签名缺失
- 结果: 全部通过

整改验收使告退 ✅
```

---

## 输出

- 验收记录: 写入任务文件
- 汇报: 发送到内务堂

---

整改验收使告退
