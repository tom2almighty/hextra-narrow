---
title: Markdown
weight: 35
sidebar:
  open: true
prev: /docs/content-management/frontmatter
next: /docs/configurations
---

Hugo Narrow 支持使用 Hugo 默认的渲染引擎 Goldmark，默认禁用上标和下标，如果你需要启用，可以根据 [Hugo 文档](https://gohugo.io/configuration/markup/#goldmark)更改相应的配置。

## GitHub Alert

Hugo Narrow 支持 GitHub 风格的 Alert 提示块，支持 Obsidian 的可折叠提示块。在 Hugo 未原生支持 Alert 之前，某些主题使用短代码提供相同的样式，比如某些主题叫 `Admonition` 短代码。

> [!NOTE]
> Obsidian 中的折叠提示块在其他编辑器中不会生效，只会显示默认的提示块。

你可以通过这种方式使用：

```markdown
> [!NOTE]
> 这是一个信息提示块。

> [!TIP]
> 这是一个提示提示块。

> [!IMPORTANT]
> 这是一个重要提示块。

> [!WARNING]
> 这是一个警告提示块。

> [!CAUTION]
> 这是一个注意提示块。

> [!NOTE] 自定义标题
> 这是自定义标题信息提示块。

> [!NOTE]- 可折叠提示块，默认折叠
> 这是自定义标题信息提示块。

> [!NOTE]+ 可折叠提示块，默认展开
> 这是自定义标题信息提示块。
```

## 数学公式

Hugo Narrow 通过 Katex 支持数学公式，支持在站点配置或者文章的头信息中更改相关参数，头信息中的参数可以覆盖 `hugo.yaml` 文件的配置，相关参数如下：

```yaml
params:
  katex:
    enabled: true        # 启用 KaTeX
    delimiters:          # 定义数学公式分隔符
      - left: "$$"
        right: "$$"
        display: true    # 块级公式
      - left: "$"
        right: "$"
        display: false   # 行内公式
      - left: "\\("
        right: "\\)"
        display: false   # 行内公式
      - left: "\\["
        right: "\\]"
        display: true    # 块级公式
```

## 图表

Hugo Narrow 使用 Mermaid 生成图表，支持在站点配置或者文章的头信息中更改相关参数，头信息中的参数可以覆盖 `hugo.yaml` 文件的配置，相关参数如下：

```yaml
params:
  mermaid:
    enabled: true
```
