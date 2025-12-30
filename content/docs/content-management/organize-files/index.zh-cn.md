---
title: 组织文件
weight: 31
sidebar:
  open: true
prev: /docs/quickstart/git-submodule
next: /docs/content-management/local-resources
---

## 文件结构

文件的组织结构会决定最终站点输出结构。Hugo 会索引 `content` 目录下的所有 markdown 文件。

## 页面包

一般比较难区分的是 `index.md` 和 `_index.md` 文件。

在区分之前需要了解一个概念 -- 页面包（Page Bundles）。页面包是一个包含内容文件（如 md 文件或者 html 文件）和相关资源（如图像资源）的目录，页面包分为分支包（branch Bundle）和叶子包（Leaf Bundle），叶子包是包含 `index.md` 文件的目录，也可以包含其他资源。叶子包位于分支的末端，不能包含子页面。而分支包（Branch Bundle）是指包含一个 `_index.md` 文件的目录，也可以包含其他资源。就像树枝，可以拥有子页面，可以包含叶子包。顶级目录无论是否存在 `_index.md` 文件，都是一个分支包，同时包含首页。

因此 `_index.md` 是页面包的索引文件，而 `index.md` 文件则是叶子包的内容文件，比如 `content/posts/_index.md` 代表文章列表页的索引页面内容，在其中输入的内容根据主题的模板输出到文章列表页的特定位置。而 `content/posts/post-1/index.md` 代表 posts 目录下的一个叶子包的内容文件。

因此如果你每一篇文章放到单独的文件夹下，可以使用 `index.md` 文件名，如：`content/posts/first-post/index.md`。如果你不打算使用文件夹，需要指定 markdown 文件名，比如：`content/posts/first-post.md`。你也可以将二者混合使用，所以下面这种方式是可行的：

{{< filetree/container >}}
  {{< filetree/folder name="content" >}}
    {{< filetree/file name="_index.md" >}}
    {{< filetree/folder name="posts" >}}
      {{< filetree/file name="_index.md" >}}
      {{< filetree/file name="post-1.md" >}}
      {{< filetree/file name="post-1.zh-cn.md" >}}
        {{< filetree/folder name="post-2" >}}
        {{< filetree/file name="index.md" >}}
        {{< /filetree/folder >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}

> [!NOTE]
>
> 访问 [Hugo 文档](https://gohugo.io/content-management/page-bundles/)了解更多细节。
