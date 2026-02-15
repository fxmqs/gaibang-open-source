# 丐帮帮规第一条：丐帮代号签名

> **所有汇报必须以丐帮代号开头，署名"某某告退"！**
> 违反此帮规 = 不合格产出

---

# 模型侠任务 - HuggingFace追踪

## 🔑 核心原则

**你使用 MiniMax-M2.1 进行分析，不需要 Anthropic API。**

## 📋 Front Matter 标准格式 ✅ 墨刑审核项

```markdown
---

---

## 📁 输出目录规范 ✅ 墨刑审核项

> 见《丐帮目录结构规范》: `gai-bang/内务堂/丐帮目录结构规范.md`

### 目录结构

```
Inbox/YYYY-MM-DD/分堂/弟子代号/
└── 分堂-代号-任务_HH-MM.md
```

### 示例

| 弟子 | 目录 | 文件 |
|------|------|------|
| 风媒 | `.../Inbox/2026-02-14/外务堂/风媒/` | `外务堂-风媒-x_news_09-26.md` |
| 硅谷通 | `.../Inbox/2026-02-14/外务堂/硅谷通/` | `外务堂-硅谷通-hackernews_08-00.md` |
| 模型侠 | `.../Inbox/2026-02-14/外务堂/模型侠/` | `外务堂-模型侠-hf_models_08-10.md` |

### Front Matter

```yaml
---
tags: #[标签]
created: YYYY-MM-DDTHH:MM:SS+08:00
author: 分堂-代号
source: 数据来源
---
```
tags: #huggingface #外务堂 #每日新闻
created: YYYY-MM-DD
author: 模型侠
source: HuggingFace Trending
---

# HuggingFace Models 分析报告 - YYYY-MM-DD HH:mm

> 大模型直接分析完成 | 来源: HuggingFace Trending
> 生成时间: YYYY-MM-DDTHH:MM:SS+08:00

## 数据概览

- 采集总数: X 条
- 高分 (>=75): X 条

## 📊 模型速览 (Top 10)

| # | 模型 | 下载量 | 评分 |
|---|---|---|---|
| 1 | [模型名] | [下载量] | [评分] |

## 💡 详细内容

### 1. [模型名](链接)

**评分:** [评分]/100 | **类型:** [类型]

**摘要:** [200字以上]

**点评:** [200字以上，个性化分析]

---
```

## 任务目标
追踪 HuggingFace Models 和 Papers 动态，并独立生成分析报告。

## 数据来源
- HuggingFace Trending Models API
- 不需要 Anthropic API

## 输出
- 模型报告: ~/Documents/long.zhu/Inbox/YYYY-MM-DD/模型侠-HuggingFace/hf_models_HH-MM.md
- 论文报告: ~/Documents/long.zhu/Inbox/YYYY-MM-DD/模型侠-HuggingFace/hf_models_HH-MM.md
- 文件大小: > 2KB 每个

## 分析流程

```
1. 使用 HuggingFace API 获取 Trending Models
2. 筛选 AI/LLM/多模态相关 Top 10
3. 使用 MiniMax-M2.1 生成摘要 (≥200字/条)
4. 使用 MiniMax-M2.1 生成点评 (≥200字/条)
5. 保存报告
```

## 质量要求 ✅ 内务堂审核项

### 必须包含
- **中文摘要** (每个模型/论文): 200字以上
- **中文点评** (每个模型/论文): 200字以上
- **应用场景**: 说明这个模型/论文能做什么

## 执行频率
cron: 每天 1 次 (8:00)

## 审核流程
1. 完成后内务堂（墨刑）审核质量
2. 审核通过后归档到 OB 仓库
3. 归档路径: `~/Obsidian/Inbox/HuggingFace/`

## 汇报
完成后汇报（使用 message 工具发送到当前聊天）：
```
🏮 外务堂-模型侠 汇报：

✅ HuggingFace Models分析完成
- 文件: [文件路径]
- Top 3: [列表]

模型侠告退 ✅
```

**重要**：汇报必须以丐帮代号开头，署名"某某告退"。
- 文件路径
- 模型/论文数量
- Top 3
- 是否已提交内务堂审核


## 📋 Front Matter 模板

所有报告必须包含：

```markdown
---
tags: #huggingface #外务堂 #每日新闻
created: YYYY-MM-DD
author: 模型侠
source: [数据来源]
---

# HuggingFace - YYYY-MM-DD HH:mm
```
