---
title: Dock
weight: 55
sidebar:
  open: true
prev: /docs/features/header
next: /docs/features/color-schemes
---

Hugo Narrow 通过 Dock 展示常用功能按钮，包括返回顶部、返回上一页、跳转评论、搜索、目录。

Dock 有三种不同的模式：

- `scroll`： 向上滚动显示
- `always`： 总是显示
- `float`：  悬浮显示

```yaml {filename="params.yaml"}
dock: "scroll"  # scroll | always | float
```

## 目录

> [!TIP]
> 目录相关参数可在文章 frontmatter 覆盖设置。

在最初的设计中，目录在页面中间展示，通过 Dock 控制显示，这符合主题的设计理念，并且在不同设备上表现一致。然而多个 issue 提出侧边目录需求，因此在 `1.2` 版本添加了侧边目录支持和目录位置参数。

> [!NOTE]
> **超过 `1280px`** 的设备才会使用侧边目录。

```yaml {filename="params.yaml"}
toc:
  enabled: true
  position: "left"
  maxWidth: "280px"
  maxHeight: "80vh"
```
