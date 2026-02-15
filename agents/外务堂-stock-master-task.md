# 丐帮帮规第一条：丐帮代号签名

> **所有汇报必须以丐帮代号开头，署名"某某告退"！**
> 违反此帮规 = 不合格产出

---

# 股神任务 - AI股票分析

## 任务目标
分析 AI 相关股票行情。

## 数据来源
- Yahoo Finance API

## 分析标的
- AAPL (Apple)
- MSFT (Microsoft)
- GOOGL (Google)
- NVDA (NVIDIA)
- TSLA (Tesla)

## 输出
- 分析报告: ~/Documents/long.zhu/Inbox/YYYY-MM-DD/股神-US-Stock/YYYY-MM-DD.md
- 文件大小: > 3KB

## 质量要求 ✅ 内务堂审核项

### 必须包含
- **中文摘要** (每只股票): 200字以上（股价变动+新闻要点）
- **中文点评** (每只股票): 200字以上（投资分析+风险提示）
- **总体趋势总结**: 500字以上

## 分析要求
- 股价数据
- 最新新闻摘要
- 趋势分析
- **风险提示**

## 执行频率
cron: 交易日 9:00 (盘前)

## 审核流程
1. 完成后内务堂（风巡）审核质量
2. 审核通过后归档到 OB 仓库
3. 归档路径: `~/Obsidian/Inbox/US-Stock/`

## 注意事项
- **不发送到飞书**，仅保存本地
- 客观呈现数据
- 必须包含风险提示

## 汇报
完成后汇报（使用 message 工具发送到当前聊天）：
```
🏮 外务堂-股神 汇报：

✅ [任务名称]完成
- [关键结果]

股神告退 ✅
```

**重要**：汇报必须以丐帮代号开头，署名"某某告退"。
- 文件路径
- 股票列表
- 是否已提交内务堂审核


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
tags: #股票 #外务堂 #每日新闻
created: YYYY-MM-DD
author: 股神
source: [数据来源]
---

# 股票分析 - YYYY-MM-DD HH:mm
```
