---
title: Markdown
weight: 35
sidebar:
  open: true
prev: /docs/content-management/frontmatter
next: /docs/configurations
---

Hugo Narrow use Goldmark to render markdown files. By default, the superscript and the subscript are disabled, you can change the parameters according to the [Hugo Documentation](https://gohugo.io/configuration/markup/#goldmark) to enable them.

## GitHub Alert

Hugo Narrow support GitHub Alert, Obsidian foldable alert also supported. Before Hugo native support it, some themes use the shortcodes named `Admonition` to provide the same style.

> [!NOTE]
> Obsidian's foldable alert will not affected at other editors, it will render as the default alert.

Use as the following:

```markdown
> [!NOTE]
> This is a note alert.

> [!TIP]
> This is a tip alert.

> [!IMPORTANT]
> This is a important alert.

> [!WARNING]
> This is a warning alert.

> [!CAUTION]
> This is a caution alert.

> [!NOTE] custom title
> This is a custom tiltle note alert.

> [!NOTE]- Foldable alert with custom title 
> This is a foldable alert, default is folded.

> [!NOTE]+ Foldable alert with custom title 
> This is a foldable alert, default is unfolded.
```

## Math Formula

Hugo Narrow supports math formula by katex, you can change the parameters at frontmatter or `hugo.yaml`, the frontmatter has higher priority, the supported parameters are following as these:

```yaml
params:
  katex:
    enabled: true        # enable KaTeX
    delimiters:          # delimiters
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

## Chart

Hugo Narrow supports charts by Mermaid, you can change the parameters at frontmatter or `hugo.yaml`, the frontmatter has higher priority, the supported parameters are following as these:

```yaml
params:
  mermaid:
    enabled: true      # enable Mermaid
```
