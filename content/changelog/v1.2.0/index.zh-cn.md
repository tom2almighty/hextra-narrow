---
title: Narrow v1.2.0
date: 2025-12-24
---

本次更新优化了大量内容，更新后推荐重新检查 Hugo 配置。

<!--more-->

## 重大变更

调整 Header 相关参数的层级, 添加目录位置参数, 具体参数变更如下:

```diff
- params:
-   logo:
-     image: ""
-     link: ""
-   stickyHeader: true
-   showThemeSwitch: true 
-   showDarkModeSwitch: true
-   showLanguageSwitch: true
-   languageSwitchMode: "dropdown"
+ params:
+   header:
+     sticky: true
+     logo:
+       image: ""
+       link: ""
+     showThemeSwitch: true 
+     showDarkMode: true
+     showLanguageSwitch: true
+     languageSwitchMode: "dropdown"
+   toc:
+     position: left # left | right | card
+     maxWidth: "280px"
+     maxHeight: "80vh"
```

## 功能增强

- 支持侧边栏目录
- 支持 Hugo Mod 形式引入主题
- 首页模块支持自定义顺序

## 重构

- 结构化站点配置
- 调整 header 相关参数的层级

### Bug 修复

- icon 模板支持填充图标
- 调整部分样式类名
