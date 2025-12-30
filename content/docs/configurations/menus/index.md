---
title: Menus
weight: 42
sidebar:
  open: true
prev: /docs/configurations/basic-config
next: /docs/configurations/multilingual
---

Hugo Narrow supports three menus：

- Main menu at header
- footer menu
- social menu

The `icon` is the icon before the title. It uses the `SVG` format and should be placed in the `hugo-narrow/assets/icons/` directory. The filename is used as the parameter value for reference.

> [!TIP]
> You can find more great icons at [Iconify Design](https://iconify.design/).

The `name` value uses the i18n translation file key by default. You can change it to any string and add the translation value in the translation file.

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
