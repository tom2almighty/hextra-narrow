---
title: Organize Files
weight: 31
sidebar:
  open: true
prev: /docs/quickstart/git-submodule
next: /docs/content-management/local-resources
---

## Contents Structure

By default, Hugo indexes all Markdown files in the `content` directory, and the contents structure determines the final site output structure.

## Page Bundles

The files that are generally confusing to distinguish are `index.md` and `_index.md`.

Before making the distinction, you need to understand a concept — **Page Bundles**. A Page Bundle is a directory that contains content files (such as md files or html files) and related resources (such as image resources). Page Bundles are divided into two types: **Branch Bundles** and **Leaf Bundles**.

A Leaf Bundle is a directory that contains an `index.md` file and zero or more resources. As the terminal node of a content branch, a Leaf Bundle cannot contain subpages.

A Branch Bundle refers to a directory that contains a `_index.md` file and zero or more resources. Just like a tree branch, it can have subpages and can contain Leaf Bundles. The top-level directory is always a Branch Bundle (regardless of whether an `_index.md` file exists in it) and also includes the homepage.

Therefore, `_index.md` is the index file of a Branch Bundle, while `index.md` is the content file of a Leaf Bundle. For example, `content/posts/_index.md` represents the index file of the the `posts` branch bundle, and the content written in it will be output to specific positions on the `posts` page according to the theme template. On the other hand, `content/posts/post-1/index.md` represents the content file of a Leaf Bundle under the `posts` directory.

Thus, if you place each article in a separate folder, you can use `index.md` as the file name, e.g., `content/posts/first-post/index.md`. If you do not intend to use a folder, you need to specify a Markdown file name directly, e.g., `content/posts/first-post.md`. You can also use both methods together, so the following approach is valid:

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
> See [Hugo Documentation](https://gohugo.io/content-management/page-bundles/) for more details.
