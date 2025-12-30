---
title: 作者
weight: 53
sidebar:
  open: true
prev: /docs/features/home
next: /docs/features/header
---

Hugo Narrow 作者信息位于首页，示例配置中 `avatar` 文件放置在 `~/static/` 目录，`icon` 值使用 `~/assets/icons/` 目录下文件名。

```yaml {filename="params.yaml"}
author:
  name: "Hugo Narrow"
  title: "A Clean and Minimal Hugo Theme"
  description: "Focused on content and user experience."
  avatar: "/images/avatar.svg"
  social:
    - name: "GitHub"
      url: "https://github.com/username"
      icon: "github"
    - name: "Twitter"
      url: "https://twitter.com/username"
      icon: "twitter"
    - name: "Email"
      url: "mailto:hello@example.com"
      icon: "email"
```

## 多语言

如果你的站点支持多种语言，在首页页面包的索引文件 `~/content/_index.md` 和翻译文件 `~/content/_index.zh-cn.md` 的头信息中设置参数，优先使用页面配置，否则会使用站点配置文件 `params.yaml` 中的配置。

```yaml {filename="content/_index.zh-cn.md"}
author:
  name: "Hugo Narrow"
  title: "A Clean and Minimal Hugo Theme"
  description: "Focused on content and user experience."
  avatar: "/images/avatar.svg"
  social:
    - name: "GitHub"
      url: "https://github.com/username"
      icon: "github"
    - name: "Twitter"
      url: "https://twitter.com/username"
      icon: "twitter"
    - name: "Email"
      url: "mailto:hello@example.com"
      icon: "email"
```
