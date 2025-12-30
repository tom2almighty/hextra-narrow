---
title: Formulas and Charts
weight: 60
sidebar:
  open: true
prev: /docs/features/analytics
next: /docs/features/codeblock
---

## Formulas

Hugo Narrwo supports formulas by [Katex](https://katex.org/).

> [!TIP]
> The parameters of Katex can be covered by the frontmatter of posts.

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

## Charts

Hugo Narrwo supports charts by [Mermaid](https://mermaid.js.org/).

> [!TIP]
> The toggle of mermaid can be covered by frontmatter of posts.
>
> ```yaml
> mermaid: true
> ```

```yaml{filename="params.yaml"}
mermaid:
  enabled: true
```
