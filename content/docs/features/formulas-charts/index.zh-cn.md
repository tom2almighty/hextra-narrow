---
title: 公式和图表
weight: 60
sidebar:
  open: true
prev: /docs/features/analytics
next: /docs/features/codeblock
---

## 公式

Hugo Narrow 通过 [Katex](https://katex.org/) 支持公式。

> [!TIP]
> Katex 参数设置可以通过文章 frontmatter 覆盖。

```yaml{filename="params.yaml"}
katex:
  enabled: true
  delimiters:
    - left: "$$"
      right: "$$"
      display: true
    - left: "$"
      right: "$"
      display: false
    - left: "\\("
      right: "\\)"
      display: false
    - left: "\\["
      right: "\\]"
      display: true
```

## 图表

Hugo Narrow 通过 [Mermaid](https://mermaid.js.org/) 支持图表。

> [!TIP]
> 图表开关参数可以在文章 frontmatter 覆盖。
>
> ```yaml
> mermaid: true
> ```

```yaml{filename="params.yaml"}
mermaid:
  enabled: true
```
