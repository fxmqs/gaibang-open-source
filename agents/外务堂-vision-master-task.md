# 视界通任务：视觉模型调研

## ⚠️ 丐帮帮规第一条

**所有汇报必须以丐帮代号开头，署名"某某告退"！**
> 违反此帮规 = 不合格产出

---

## 任务目标
调研文生图和文生视频模型，产出调研报告。

## 数据来源

| 类别 | 来源 | 方式 |
|------|------|------|
| 文生图模型 | HuggingFace, GitHub, X | web search |
| 文生视频模型 | HuggingFace, Replicate, X | web search |
| 视觉模型动态 | 行业新闻, 学术论文 | web search |

## 调研内容

### 1. 文生图模型
- 主流 Text-to-Image 模型
- 风格特点对比
- 在线体验链接
- 许可证/价格

### 2. 文生视频模型
- 主流 Text-to-Video 模型
- 画质/速度对比
- 工具链配置
- 应用场景

### 3. 行业趋势
- 技术发展方向
- 商业化进展
- 开源/闭源对比

## 输出
- 报告路径: ~/Documents/long.zhu/Inbox/YYYY-MM-DD/视界通-Vision/YYYY-MM-DD.md
- 文件大小: > 3KB

## 调研流程

```
1. 使用 web search 搜索文生图模型
2. 使用 web search 搜索文生视频模型
3. 筛选 Top 5-10 个主流模型
4. 整理信息：名称、特点、价格、链接
5. 使用 MiniMax-M2.1 生成分析
6. 保存报告
```

## 质量要求

- ✅ 每个模型有简要描述
- ✅ 包含使用链接
- ✅ 对比分析表格
- ✅ 趋势总结

## 汇报
```
🏮 外务堂-视界通 汇报：

✅ 视觉模型调研完成
- 纹身图模型: X 个
- 纹身视频模型: X 个
- 报告路径: [文件路径]
- 文件大小: [大小] 字节

视界通告退 ✅
```

## cron
每周一 9:00

## 提交审核
完成后提交内务堂（墨刑）审核


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
tags: #视觉模型 #外务堂 #每日新闻
created: YYYY-MM-DD
author: 视界通
source: [数据来源]
---

# 视觉模型调研 - YYYY-MM-DD HH:mm
```
