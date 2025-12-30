---
title: Codeblock
weight: 61
sidebar:
  open: true
prev: /docs/features/formulas-charts
next: /docs/features/gallery
---

Hugo Narrow add kinds of functions for codeblock:

- click to copy
- code language display
- collapse codeblock

```yaml {filename="params.yaml"}
codeblock:
  collapse:
    enabled: true
    defaultState: expanded  # expanded, collapsed
    autoCollapseLines: 30
    autoCollapseHeight: 400
    collapsedHeight: 120
```

## Highlight

Hugo Narrow uses `chroma` for syntax highlighting, with `github` and `github-dark` as the styles for light and dark modes respectively.

To better integrate with the theme, the style files are created and adapted using the command `hugo gen chromastyles --style=github > ./assets/css/github.css`. Modifying the highlighting styles also requires generating them via the command line, making the process of replacing them somewhat complex:

1. Generate the styles using the `hugo cli`.
2. Replace the corresponding theme variable colors in `~/assets/css/chroma.css`.

```bash
# view all chroma styles
hugo gen chromastyles --help

# generate style files
hugo gen chromastyles --style=github > ./github.css
hugo gen chromastyles --style=github-dark > ./github-dark.css
```
