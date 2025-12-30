---
title: Posts
weight: 57
sidebar:
  open: true
prev: /docs/features/color-schemes
next: /docs/features/comments
---

Hugo Narrow supports configure the license of posts and the related posts.

> [!TIP]
> The parameters of license could cover by posts frontmatter.

```yaml {filename="params.yaml"}
post:
  showRelated: true 
  relatedPostsCount: 3
  license:
    show: true
    author: "Hugo Narrow"
    name: "CC BY-NC-SA 4.0"
    description: "This work is licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License. Please attribute the source, use non-commercially, and maintain the same license."
    url: "https://creativecommons.org/licenses/by-nc-sa/4.0/"
    displayName: "CC BY-NC-SA 4.0"
```
