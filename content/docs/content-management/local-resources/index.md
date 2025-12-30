---
title: Local Resources
weight: 32
sidebar:
  open: true
prev: /docs/content-management/organize-files
next: /docs/content-management/archetypes
---


Hugo Narrow support import local resources such as images with three methods:

- Page Bundles (markdown folder)
- Global Resources (assets folder)
- Static Resources (static folder)

> [!TIP]
>
> Hugo Narrow follow the order to index the local resources：Page Bundles > Global Resources > Static Resources

## Page Bundles

Page Bundles refer to resource files located in the same directory as the Markdown file. This is the most recommended method for managing image resources.

{{< filetree/container >}}
  {{< filetree/folder name="content" >}}
    {{< filetree/folder name="posts" >}}
      {{< filetree/file name="post-1.md" >}}
      {{< filetree/file name="post-1.zh-cn.md" >}}
        {{< filetree/folder name="post-2" >}}
        {{< filetree/file name="index.md" >}}
        {{< filetree/file name="index.zh-cn.md" >}}
        {{< filetree/file name="featured.jpg" >}}
          {{< filetree/folder name="gallery" >}}
          {{< filetree/file name="image-1.jpg" >}}
          {{< filetree/file name="image-2.jpg" >}}
          {{< /filetree/folder >}}
        {{< /filetree/folder >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}

Use in Markdown:

```markdown
![](featured.jpg)
![](gallery/image-1.jpg)
![](gallery/image-2.jpg)
```

> [!NOTE]
>
> See [Hugo documentation](https://gohugo.io/content-management/page-bundles/) for more details.

## Global Resources

Global resources are placed in the assets folder at the root directory of the site: `~/assets/`. Resources placed in this folder will be **processed** by Hugo during the build.

{{< filetree/container >}}
  {{< filetree/folder name="my-site" >}}
    {{< filetree/folder name="assets" >}}
      {{< filetree/folder name="images" >}}
      {{< filetree/file name="hero.jpg" >}}
      {{< /filetree/folder >}}
    {{< /filetree/folder >}}
    {{< filetree/folder name="content" state="closed" >}}
    {{< /filetree/folder >}}
    {{< filetree/folder name="themes" >}}
      {{< filetree/folder name="hugo-narrow" state="closed" >}}
      {{< /filetree/folder >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}

Use in Markdown:

```markdown
![](images/hero.jpg)
```

> [!NOTE]
>
> See [Hugo documentation](https://gohugo.io/quick-reference/glossary/#global-resource) for more details.

## Static Resources

Static resources are placed in the assets folder at the root directory of the site: `~/static/`. Resources placed in this folder will **NOT** be processed by Hugo during the build.

{{< filetree/container >}}
  {{< filetree/folder name="my-site" >}}
    {{< filetree/folder name="static" >}}
      {{< filetree/folder name="images" >}}
      {{< filetree/file name="hero.jpg" >}}
      {{< /filetree/folder >}}
    {{< /filetree/folder >}}
    {{< filetree/folder name="content" state="closed" >}}
    {{< /filetree/folder >}}
    {{< filetree/folder name="themes" >}}
      {{< filetree/folder name="hugo-narrow" state="closed" >}}
      {{< /filetree/folder >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}

Use in Markdown:

```markdown
![](/images/hero.jpg)
```

> [!NOTE]
>
> See [Hugo documentation](https://gohugo.io/getting-started/directory-structure/#static) for more details.

## Different

|                  |                Location               |      Use               |
| ---------------- | :------------------------------------ | ---------------------- |
| Page Bundles     | `~/content/posts/post-1/featured.jpg` | `featured.jpg`         |
| Global Resources | `~/assets/images/featured.jpg`        | `images/featured.jpg`  |
| Static Resources | `~/static/images/featured.jpg`        | `/images/featured.jpg` |

> [!NOTE]
>
> `images` is not necessary, you can change it.
