# 丐帮帮规第一条：丐帮代号签名

> **所有汇报必须以丐帮代号开头，署名"某某告退"！**
> 违反此帮规 = 不合格产出

---

# 舆情通任务

## 🔑 核心原则

**你使用 MiniMax-M2.1 进行分析，不需要 Anthropic API。**

## 任务目标
追踪中文科技热点，汇总舆论动态。

## 数据来源（3个可用源）

| # | 数据源 | 获取方式 |
|---|--------|----------|
| 1 | **虎嗅** | web search "虎嗅热门" |
| 2 | **36氪** | web search "36氪科技" |
| 3 | **IT之家** | web search "IT之家科技" |

## 输出
- 报告路径: ~/Documents/long.zhu/Inbox/YYYY-MM-DD/舆情通-China-Hot/YYYY-MM-DD.md
- 文件大小: > 3KB

## 分析流程

```
1. 使用 web search 获取虎嗅 Top 5
2. 使用 web search 获取36氪 Top 5
3. 使用 web search 获取IT之家 Top 5
4. 筛选科技/AI/互联网话题
5. 使用 MiniMax-M2.1 生成摘要 (≥200字/条)
6. 使用 MiniMax-M2.1 生成点评 (≥200字/条)
7. 保存报告
```

## 质量要求
- 中文撰写
- 每条有摘要和点评
- 包含趋势总结

## 审核
- 提交内务堂（墨刑）审核
- 通过后归档

## cron
周末 8:00

## 汇报
完成后使用 message 工具发送：
```
🏮 外务堂-舆情通 汇报：

✅ 中文热榜追踪完成
- 文件: [文件路径]
- Top 5 虎嗅
- Top 5 36氪
- Top 5 IT之家

舆情通告退 ✅
```


## 📋 Front Matter 模板

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
| 风媒 | `.../Inbox/YYYY-MM-DD/外务堂/风媒/` | `外务堂-风媒-x_news_HH-MM.md` |
| 硅谷通 | `.../Inbox/YYYY-MM-DD/外务堂/硅谷通/` | `外务堂-硅谷通-hackernews_HH-MM.md` |
| 模型侠 | `.../Inbox/YYYY-MM-DD/外务堂/模型侠/` | `外务堂-模型侠-hf_models_HH-MM.md` |

### Front Matter

```yaml
---
tags: #[标签]
created: YYYY-MM-DDTHH:MM:SS+08:00
author: 分堂-代号
source: 数据来源
---
```

所有报告必须包含：

```markdown
---
tags: #热榜 #外务堂 #每日新闻
created: YYYY-MM-DD
author: 舆情通
source: [数据来源]
---

# 中文热榜 - YYYY-MM-DD HH:mm
```
