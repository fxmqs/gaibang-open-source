# 丐帮帮规第一条：丐帮代号签名

> **所有汇报必须以丐帮代号开头，署名"某某告退"！**
> 违反此帮规 = 不合格产出

---

# 建设堂任务 - 分堂建设

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

建设丐帮四大分堂，创建必要弟子和 cron 任务。

## 四大分堂

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


### 1. 外务堂（已建 2/6）
- [x] xnews-collector - X 新闻采集
- [x] xnews-analyzer - X 新闻分析
- [x] hackernews-analyzer - HackerNews 分析
- [ ] github-trending - GitHub 趋势采集
- [ ] hf-collector - HuggingFace 采集
- [ ] stock-analyzer - 股票分析

### 2. 内务堂（已建 1/3）
- [x] cron-inspector - 定时任务监控
- [ ] system-monitor - 系统状态监控
- [ ] memory-manager - 记忆管理

### 3. 建设堂（已建 1/2）
- [x] construction-master - 建设堂堂主（你）
- [ ] skill-developer - Skill 开发者
- [ ] agent-creator - Agent 创建者

### 4. 财务堂（未来）
- [ ] 商业分析师
- [ ] 投资顾问

## 你的任务

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


### 第一阶段：完善外务堂
1. 创建 github-trending 弟子
   - 职责：采集 GitHub Trending
   - 状态：cron 脚本已有，需要 sub-agent
   - 路径：`~/Documents/long.zhu/Inbox/YYYY-MM-DD/GitHub/`

2. 创建 hf-collector 弟子
   - 职责：采集 HuggingFace Models/Papers
   - 状态：cron 脚本已有，需要 sub-agent
   - 路径：`~/Documents/long.zhu/Inbox/YYYY-MM-DD/HuggingFace/`

3. 创建 stock-analyzer 弟子
   - 职责：股票分析
   - 状态：cron 已有，需要 sub-agent
   - 路径：`~/Documents/long.zhu/Inbox/YYYY-MM-DD/US-Stock/`

### 第二阶段：完善内务堂
1. 创建 system-monitor 弟子
   - 职责：监控 Gateway、CPU、内存
   - 输出：system_status_YYYY-MM-DD.md

2. 创建 memory-manager 弟子
   - 职责：定期整理 memory 文件
   - 输出：更新 MEMORY.md

### 第三阶段：完善建设堂
1. 创建 skill-developer 弟子
   - 职责：开发新 Skill
   - 产出：新 Skill 文件

2. 创建 agent-creator 弟子
   - 职责：创建新 Agent
   - 产出：新 Agent 文件

---

## 重构人设流程

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


当需要重构弟子人设时，遵循以下步骤：

### 第一步：评估现有结构
检查目标弟子的文件：
- SOUL.md（人设）
- IDENTITY.md（身份）
- agent.json（配置）
- task.md（任务流程）

### 第二步：执行重构

#### 1. 重构 SOUL.md（必须 ≤200行）
- **角色定位**（简洁描述弟子定位）
- **沟通风格**（简洁描述语气风格）
- **核心职责**（列出3-5条核心职责）
- **边界约束**（包含禁止事项）

#### 2. 创建 IDENTITY.md
```markdown
- Name: 弟子代号
- Emoji: 代表 emoji
- Vibe: 风格描述
```

#### 3. 清理 agent.json
- **移除** `defaultModel` 字段（使用全局配置）
- **移除** `systemPrompt` 字段（应该在 SOUL.md 中）
- **保留** `agentId`、`name`、`description`

#### 4. 独立 task.md
- 将任务流程移到 task.md
- SOUL.md 只保留人设

### 第三步：验证标准
- [ ] SOUL.md ≤200行
- [ ] 角色定位、沟通风格、核心职责、边界约束完整
- [ ] IDENTITY.md 包含 Name、Emoji、Vibe
- [ ] agent.json 无 defaultModel（使用全局配置）
- [ ] task.md 包含任务流程

### 第四步：汇报格式
重构完成后汇报：
```
✅ [弟子名称] 人设重构完成
- SOUL.md: X 行
- IDENTITY.md: Y bytes
- agent.json: 已清理 defaultModel
- task.md: 已独立
```

---

## 弟子模板

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


### 最小 Agent 结构
```
agents/{agent-name}/
├── SOUL.md          # Agent 人格（必须 ≤200行）
├── IDENTITY.md      # 身份标识
├── agent.json       # Agent 配置（无 defaultModel）
└── task.md          # 任务指令

```

### agent.json 标准模板
```json
{
  "agentId": "agent-name",
  "name": "弟子名",
  "description": "...",
  "enabled": true
}
```

### Cron 任务结构
```json
{
  "agentId": "{agent-name}",
  "name": "{任务名称}",
  "schedule": "{cron 表达式}",
  "sessionTarget": "isolated",
  "payload": {
    "kind": "agentTurn",
    "message": "任务描述..."
  }
}
```

---

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


完成后汇报：
- 创建的弟子列表
- 配置的 cron 任务
- 建设进度（X/Y 完成）
- 下一步计划
