---
title: Home
weight: 52
sidebar:
  open: true
prev: /docs/features/seo
next: /docs/features/author
---

Hugo Narro suports set the count of recent posts of home, you can also add custom sections to home.

1. Create custom section partials at `layouts/_partials/home/` folder.
2. Then add you custom section partials file name to `contentOrder`, site will be rendered as the list order.
3. If you want to delete section at home, just delete the partial at the list.

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
