# 丐帮帮规第一条：丐帮代号签名

> **所有汇报必须以丐帮代号开头，署名"某某告退"！**
> 违反此帮规 = 不合格产出

---

# 铜铃任务 - 系统监控

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

监控丐帮系统运行状态，及时发现异常。

## 监控内容

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


### 1. Gateway 状态
- 运行状态
- 最后重启时间
- 异常记录

### 2. Cron 任务
- 今日执行次数
- 成功/失败统计
- 失败任务清单

### 3. 系统资源
- CPU 使用率
- 内存使用率
- 磁盘使用率

## 输出

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


### 每日健康报告
```
📋 系统健康报告 - [日期]

🔧 Gateway 状态
- 状态: 运行中/异常
- 最后重启: [时间]

📊 Cron 执行统计
- 总任务: X
- 成功: X
- 失败: X
- 成功率: X%

💻 系统资源
- CPU: X%
- 内存: X%
- 磁盘: X%

⚠️ 异常记录
- 任务1: 问题描述
- 任务2: 问题描述
```

## 执行频率

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

cron: 每 5 分钟

## 告警规则

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


| 级别 | 触发条件 | 处理 |
|------|----------|------|
| 🔴 严重 | Gateway 停止 | 立即汇报 |
| 🟡 警告 | Cron 成功率 < 80% | 记录汇报 |
| 🟢 正常 | 其他 | 仅记录 |

## 汇报模板

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


```
📋 系统监控报告 - [时间]

✅ 正常项
- 项目1
- 项目2

⚠️ 异常项
- 项目1: 问题描述
- 项目2: 问题描述

🎯 建议
- 建议1
- 建议2
```
