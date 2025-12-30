---
title: 导航菜单
weight: 42
sidebar:
  open: true
prev: /docs/configurations/basic-config
next: /docs/configurations/multilingual
---

Hugo Narrow 支持三处导航菜单：

- 顶部菜单（main）
- 页脚菜单（footer）
- 社交链接菜单（social）

其中 `icon` 为标题前图标，使用 `SVG` 格式，放置在 `hugo-narrow/assets/icons/` 目录下，使用文件名作为参数值引用。

> [!TIP]
> 可以在 [Iconify Design](https://iconify.design/) 找到更多优质图标。

`name` 值默认使用 i18n 翻译文件键值，你可以更改为任意字符串，并在翻译文件中添加翻译值。

```yaml {filename="exampleSite/config/_default/menus.yaml"}
main:
  - name: nav.posts
    pageRef: /posts
    weight: 20
    params:
      icon: posts
  - name: nav.projects
    pageRef: /projects
    weight: 25
    params:
      icon: projects
  - name: nav.categories
    pageRef: /categories
    weight: 30
    params:
      icon: categories
  - name: nav.tags
    pageRef: /tags
    weight: 40
    params:
      icon: tags
  - name: nav.archives
    pageRef: /archives
    weight: 50
    params:
      icon: archive

# footer menu
footer:
  - name: About
    pageRef: /about
    weight: 10
    params:
      icon: about
  - name: Contact
    url: https://google.com
    weight: 20
    params:
      icon: contact
  - name: RSS Feed
    url: /index.xml
    weight: 30
    params:
      icon: rss

# social link
social:
  - name: GitHub
    url: https://github.com/username
    weight: 10
    params:
      icon: github
  - name: Twitter
    url: https://twitter.com/username
    weight: 20
    params:
      icon: twitter
  - name: LinkedIn
    url: https://linkedin.com/in/username
    weight: 30
    params:
      icon: linkedin
  - name: Email
    url: mailto:your.email@example.com
    weight: 40
    params:
      icon: email

```
