---
title: Author
weight: 53
sidebar:
  open: true
prev: /docs/features/home
next: /docs/features/header
---

Hugo Narrow author information render at hoempage, in the sample configuration, the `avatar` file is placed in the `~/static/` directory. `icon` value uses the file name of `~/assets/icons/` directory.

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

## Multilingual

If your site supports multiple languages, set parameters in the front matter of the index file `~/content/_index.md` and the translation file `~/content/_index.zh-cn.md` of the home page bundle. Page configurations are prioritized; otherwise, configurations from the site configuration file `params.yaml` will be used.

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
