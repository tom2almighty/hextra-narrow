---
title: 首页
weight: 52
sidebar:
  open: true
prev: /docs/features/seo
next: /docs/features/author
---

首页支持设置最近文章数量和首页模块顺序，并可以添加自定义模块。

1. 在 `layouts/_partials/home/` 目录创建模板文件。
2. 在 `contentOrder` 列表添加模板文件名，首页各部分内容会按照列表顺序渲染。
3. 如果你想去除某个模块，在列表中删除对应模板名称即可。

```yaml {filename="params.yaml"}
home:
  recentPostsCount: 5
  contentOrder:
    - author-section
    - custom_1.html
    - featured-projects.html
    - recent-posts
    - page-content
```
