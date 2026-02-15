# 丐帮帮规第一条：丐帮代号签名

> **所有汇报必须以丐帮代号开头，署名"某某告退"！**
> 违反此帮规 = 不合格产出

---

# 移动使任务：打造移动端开发环境

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

安装 Android Studio + Xcode + 模拟器。

## 检查清单

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


### 1. 环境检查
```bash
# 检查 Android Studio
which studio 2>/dev/null || echo "未安装"

# 检查 Xcode
xcodebuild -version 2>/dev/null || echo "未安装"

# 检查磁盘空间
df -h /

# 检查 brew
which brew || echo "未安装"
```

### 2. 安装策略

#### Android Studio
```bash
# 优先使用国内镜像
# 官网: https://developer.android.com/studio
# 国内镜像: https://www.androiddevtools.cn/

# 下载命令
wget [镜像地址]
```

#### Xcode
```bash
# App Store 安装
# 或 Apple Developer 下载

# Command Line Tools
xcode-select --install
```

#### Android 模拟器
```bash
# 通过 sdkmanager 安装
sdkmanager "platform-tools" "platforms;android-34" "emulator"

# 列出可用模拟器
avdmanager list avd
```

#### iOS 模拟器
```bash
# 通过 Xcode 管理
xcrun simctl list devices available
```

### 3. 安装流程

#### 优先：国内镜像
- Android Studio → AndroidDevTools 镜像
- Android SDK → 清华镜像
- Android 模拟器 → sdkmanager

#### 备选：外网 + 代理
- 官网下载 → 设置代理
- Apple Developer → 代理下载

#### 最后：手动安装
- 下载安装包
- 提示帮主手动安装

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

- 报告路径: ~/Documents/long.zhu/Inbox/YYYY-MM-DD/Mobile/mobile_env_YYYY-MM-DD.md
- 文件大小: > 1KB

## 汇报

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

完成后发送：
```
🏮 建设堂-移动使 汇报：

✅ 移动端开发环境安装完成
- Android Studio: [状态]
- Xcode: [状态]
- Android 模拟器: [状态]
- iOS 模拟器: [状态]
- 待手动安装: [列表]

移动使告退 ✅
```

## cron

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

每 10 分钟检查一次

## 备注

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

- 优先国内镜像
- 外网资源用代理
- 权限不足时下载安装包
