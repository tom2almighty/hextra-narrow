---
title: Narrow v1.1.2
date: 2025-07-02
---

本次更新优化了文章版权信息参数。

<!--more-->

## Bug 修复

- 修复 Frontmatter 版权参数不生效

## 样式优化

- 图片居中显示

## 重大变更

- license 字段添加 `author` 和 `show` 参数
- 删除 `showLicense` 参数

```diff
params:
  post:
-   showLicense: true
    license:
+     show: true
+     author: "Hugo Narrow"
      name: "CC BY-NC-SA 4.0"
      description: "This work is licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License. Please attribute the source, use non-commercially, and maintain the same license."
      url: "https://creativecommons.org/licenses/by-nc-sa/4.0/"
      displayName: "CC BY-NC-SA 4.0"
```
