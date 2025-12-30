---
title: Narrow v1.1.5
date: 2025-09-05
---

本次更新添加了 dock 显示模式参数，优化部分样式。

<!--more-->

## 功能增强

- 使用新标签页打开外部链接
- 支持自定义 js 文件
- 添加 404 模板
- 添加 dock 显示模式参数

```diff
params
+  dock: float # Options: "scroll" (show on scroll up), "always" (always visible), "float" (floating)
```

## 样式优化

- 修改上标下标颜色
- 修改 alert 引用块底部 padding
