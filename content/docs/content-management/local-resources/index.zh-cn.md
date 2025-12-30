---
title: 本地资源
weight: 32
sidebar:
  open: true
prev: /docs/content-management/organize-files
next: /docs/content-management/archetypes
---



Hugo Narrow 支持多种方式引入本地资源如图像：

- 页面资源（markdown 文件所在目录下）
- 全局资源（assets 目录下）
- 静态资源（static 目录下）

> [!TIP]
>
> Hugo Narrow 本地资源查找遵循以下顺序：页面资源 > 全局资源 > 静态资源

## 页面资源

页面资源是指与 Markdown 文件位于同一目录下的资源文件。这是最推荐的图像资源管理方式。

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

在 Markdown 中引用：

```markdown
![](featured.jpg)
![](gallery/image-1.jpg)
![](gallery/image-2.jpg)
```

> [!NOTE]
>
> 访问 [Hugo 文档](https://gohugo.io/content-management/page-bundles/) 了解更多细节。

## 全局资源

全局资源是放置在站点根目录下的 `assets` 文件夹： `~/assets/`，放置在这个文件夹下的资源在构建时**会**被 Hugo 处理。

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

在 Markdown 中引用：

```markdown
![](images/hero.jpg)
```

> [!NOTE]
>
> 访问 [Hugo 文档](https://gohugo.io/quick-reference/glossary/#global-resource) 了解更多细节。

## 静态资源

静态资源是放置在站点根目录下的 `static` 文件夹： `~/static/`，放置在这个文件夹下的资源在构建时**不会**被 Hugo 处理。

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

在 Markdown 中引用：

```markdown
![](/images/hero.jpg)
```

> [!NOTE]
>
> 访问 [Hugo 文档](https://gohugo.io/getting-started/directory-structure/#static) 了解更多细节。

## 引用区别

|          | 位置                                  | 引入方式               |
| -------- | ------------------------------------- | ---------------------- |
| 页面资源 | `~/content/posts/post-1/featured.jpg` | `featured.jpg`         |
| 全局资源 | `~/assets/images/featured.jpg`        | `images/featured.jpg`  |
| 静态资源 | `~/static/images/featured.jpg`        | `/images/featured.jpg` |

> [!NOTE]
>
> 其中 `images` 路径不是必须，可以自行更改。
