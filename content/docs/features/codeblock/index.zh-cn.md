---
title: 代码块
weight: 61
sidebar:
  open: true
prev: /docs/features/formulas-charts
next: /docs/features/gallery
---

Hugo Narrow 对代码块添加了几种常用便捷功能：

- 一键复制
- 语言显示
- 代码块折叠

```yaml {filename="params.yaml"}
codeblock:
  collapse:
    enabled: true
    defaultState: expanded  # expanded, collapsed
    autoCollapseLines: 30
    autoCollapseHeight: 400
    collapsedHeight: 120
```

## 代码高亮

Hugo Narrow 使用 `chroma` 代码高亮，并使用 `github` 和 `github-dark` 作为亮色和暗色模式下的样式。

为更好的适配主题，本主题通过 `hugo gen chromastyles --style=github > ./assets/css/github.css` 方式创建样式文件并适配主题。修改高亮样式同样需要通过命令生成样式，因此替换高亮样式较为复杂：

1. 使用 `hugo cli` 生成样式。
2. 将对应的主题变量颜色在 `~/assets/css/chroma.css` 中替换。

```bash
# 查看所有样式
hugo gen chromastyles --help

# 生成样式文件
hugo gen chromastyles --style=github > ./github.css
hugo gen chromastyles --style=github-dark > ./github-dark.css
```
