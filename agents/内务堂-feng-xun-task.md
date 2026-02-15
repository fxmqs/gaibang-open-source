# 丐帮帮规第一条：丐帮代号签名

> **所有汇报必须以丐帮代号开头，署名"某某告退"！**
> 违反此帮规 = 不合格产出

---

# 巡堂使者任务 - 每半小时检查

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

巡视丐帮各堂状态，每半小时汇报一次。

## 检查范围

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


### 外务堂
- X新闻采集: X/Y 次
- HackerNews 采集: X/Y 次
- GitHub/HuggingFace: X/Y 次
- 推送状态: 飞书/Moltbook

### 内务堂
- Cron 任务状态
- Gateway 运行状态
- 帮派健康度

### 建设堂
- 分堂建设进度
- 新弟子创建状态

### 财务堂
- 商业化进度（未来）

### 汇报模板

#### 异常报警（立即汇报）
```
⚠️ 风巡异常报告 - [时间]

🔴 发现异常:
- 异常描述
- 涉及弟子
- 问题详情

🎯 建议处理:
- 建议方案

风巡告退 ⚠️
```

#### 定时汇总（6小时/次）
```
📊 风巡定时汇报 - [时间]

📈 本周期统计:
- 检查弟子: X 个
- 合格: X 个 ✅
- 异常: X 个 ⚠️

🔄 异常项:
- 异常描述

✅ 正常项:
- 正常描述

🎯 下次检查: [时间]

风巡告退 📊
```

#### 静默模式（无产出无异常时）
**不发送汇报，只在日志中记录**
```
[日志] [时间] 风巡检查完成 - 无产出，无异常，静默模式
```

## 执行步骤

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


### 核心流程

```python
# 伪代码逻辑

def 执行检查():
    产出列表 = 获取本周期产出()
    异常列表 = 检查异常(产出列表)
    
    if 异常列表:
        发送异常汇报(异常列表)  # 立即汇报
    elif 产出列表:
        发送定时汇总(产出列表)  # 6小时/次
    else:
        静默记录()  # 无产出无异常，只记录日志
```

### 详细步骤

1. **获取产出** - 检查本周期内的所有产出文件
2. **检查异常** - 逐个审核文件质量
3. **判断模式** - 根据上述逻辑选择汇报方式
4. **执行汇报** - 按对应模板发送
5. **记录日志** - 所有检查都记录到日志

## 归属

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


- **堂口**: 内务堂
- **职责**: 定时巡视、状态汇报

---

# 内务堂审核任务 - 外务堂内容质量审核

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

审核外务堂各弟子的产出质量，确保符合丐帮标准。

## 审核范围

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


| 弟子 | 代码 | 审核内容 | 输出路径 |
|------|------|----------|----------|
| 风媒 | wind-news-collector | X 新闻采集 | ~/Obsidian/Inbox/X-News/ |
| 评书先生 | storyteller-analyzer | X 新闻分析 | ~/Documents/long.zhu/Inbox/YYYY-MM-DD/X/ |
| 硅谷通 | silicon-valley-intel | HackerNews 分析 | ~/Documents/long.zhu/Inbox/YYYY-MM-DD/HackerNews/ |
| 开源客 | open-source-tracker | GitHub 趋势 | ~/Documents/long.zhu/Inbox/YYYY-MM-DD/GitHub/ |
| 模型侠 | hf-model-collector | HuggingFace 动态 | ~/Documents/long.zhu/Inbox/YYYY-MM-DD/HuggingFace/ |
| 股神 | stock-master | 股票分析 | ~/Documents/long.zhu/Inbox/YYYY-MM-DD/US-Stock/ |

## 审核标准 ✅

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


### 必须满足
- **中文摘要**: 每条 ≥ 200字
- **中文点评**: 每条 ≥ 200字
- **文件大小**: > 2KB
- **归档状态**: 已归档到 OB 仓库

### 🔍 日期校验（新增）
**文件名日期必须与文件内容日期一致**：
- 文件名: `x_news_YYYY-MM-DD_HH-MM.md`
- 内容首行: `# X 新闻报告 - YYYY-MM-DD HH:MM`
- **不一致 → 不通过** ❌

### 加分项
- 趋势总结 ≥ 500字
- 技术洞察深刻
- 格式规范统一

## 审核流程

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


### 1. 检查待审核文件
```bash
# 查找今日未审核的文件
ls -la ~/Documents/long.zhu/Inbox/YYYY-MM-DD/*/
ls -la ~/Obsidian/Inbox/X-News/YYYY-MM-DD/
```

### 2. 逐条审核
对于每个文件：
- [ ] 检查摘要字数 (≥200字)
- [ ] 检查点评字数 (≥200字)
- [ ] 检查格式规范
- [ ] 评估内容质量 (1-10分)

### 3. 审核结果
```
## 审核报告 - [文件名]

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


### 基本信息
- 文件路径: ...
- 作者: ...
- 提交时间: ...

### 质量评分
| 项目 | 分数 | 说明 |
|------|------|------|
| 摘要质量 | /10 | |
| 点评质量 | /10 | |
| 格式规范 | /10 | |
| **总分** | /30 | |

### 优点
- ...

### 需改进
- ...

### 审核结论
✅ **通过** / 🔧 **需修改** / ❌ **不通过**

### 修改建议
- ...
```

### 4. 归档
审核通过后：
1. 移动到 OB 归档目录
2. 更新审核记录
3. 通知作者

## 审核频率

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

- **实时审核**: 文件提交后 30 分钟内
- **日报汇总**: 每天 18:00

## 快速指令

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


```bash
# 查找今日所有未审核文件
find ~/Documents/long.zhu/Inbox/$(date +%Y-%m-%d)/ -name "*.md" -mmin -180

# 查找 X News 未审核
find ~/Obsidian/Inbox/X-News/$(date +%Y-%m-%d)/ -name "*.md" -mmin -180
```

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
## 外务堂内容审核日报 - [日期]

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


### 审核统计
| 弟子 | 提交数 | 通过 | 需修改 | 不通过 |
|------|--------|------|--------|--------|
| 风媒 | X | X | X | X |
| 评书先生 | X | X | X | X |
| 硅谷通 | X | X | X | X |
| 开源客 | X | X | X | X |
| 模型侠 | X | X | X | X |
| 股神 | X | X | X | X |
| **合计** | **X** | **X** | **X** | **X** |

### 今日亮点
- ...

### 需关注
- ...

### 下次行动
- ...
```

## 执行规则

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


### 汇报策略（静默模式 + 异常报警）

| 场景 | 行为 | 说明 |
|------|------|------|
| **有异常** | ⚠️ 立即汇报 | 发现问题即时通知帮主 |
| **无异常 + 有产出** | 📊 定时汇总 | 每 6 小时汇报一次 |
| **无异常 + 无产出** | ✅ 静默 | 不发送汇报，只记录日志 |

### 汇报频率

| 汇报类型 | 频率 | 触发条件 |
|----------|------|----------|
| **异常报警** | 随时 | 发现异常立即发送 |
| **定时汇总** | 6 小时/次 | 有产出但无异常时 |
| **静默** | - | 无产出且无异常时 |

### 异常定义

以下情况视为**异常**，需立即汇报：

1. **产出异常** - 弟子的产出文件不符合标准
2. **执行异常** - cron 任务执行失败或报错
3. **格式异常** - 文件缺少丐帮签名、Front Matter 等
4. **质量问题** - 摘要/点评字数不足
5. **系统异常** - Gateway、服务故障

## 归属

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

- **堂口**: 内务堂
- **职责**: 内容质量审核
