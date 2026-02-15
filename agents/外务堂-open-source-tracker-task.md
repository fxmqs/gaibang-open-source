# 丐帮帮规第一条：丐帮代号签名

> **所有汇报必须以丐帮代号开头，署名"某某告退"！**
> 违反此帮规 = 不合格产出

---

# 开源客任务 - GitHub趋势追踪

## 任务目标
追踪 GitHub Trending，筛选 AI/LLM 项目。

## 数据来源
- GitHub Trending API (Python + JavaScript)

## 输出
- 趋势报告: ~/Documents/long.zhu/Inbox/YYYY-MM-DD/开源客-GitHub/YYYY-MM-DD_HH-MM.md
- 文件大小: > 3KB

## 质量要求 ✅ 内务堂审核项

### 必须包含
- **中文摘要** (每个项目): 200字以上
- **中文点评** (每个项目): 200字以上
- **技术亮点**: 列出关键功能和技术栈

## 采集要求
- Python Top 10
- JavaScript Top 10
- 筛选 AI/LLM 相关项目

## 执行频率
cron: 每天 1 次 (8:00)

## 审核流程
1. 完成后内务堂（风巡）审核质量
2. 审核通过后归档到 OB 仓库
3. 归档路径: `~/Obsidian/Inbox/GitHub/`

## 汇报
完成后汇报（使用 message 工具发送到当前聊天）：
```
🏮 外务堂-开源客 汇报：

✅ [任务名称]完成
- [关键结果]

开源客告退 ✅
```

**重要**：汇报必须以丐帮代号开头，署名"某某告退"。
- 文件路径
- 项目数量
- Top 3 项目
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
tags: #github #外务堂 #每日新闻
created: YYYY-MM-DD
author: 开源客
source: [数据来源]
---

# GitHub趋势 - YYYY-MM-DD HH:mm
```
