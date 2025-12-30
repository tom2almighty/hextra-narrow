---
title: Narrow v1.1.6
date: 2025-11-16
---

本次更新首页内容添加自定义模板。

<!--more-->

## 功能增强

- 首页作者信息支持 i18n 翻译
- 首页作者信息和最近文章之间添加自定义内容模板

```diff
+ params:
+   home_custom:
+   enabled: true
+     files:
+       - custom_1.html
+       - custom_2.html
```

## Bug 修复

- 修复站点配置文件中 clarity 参数名称错误
