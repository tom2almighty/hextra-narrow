---
title: 内容模板
weight: 33
sidebar:
  open: true
prev: /docs/content-management/local-resources
next: /docs/content-management/frontmatter
---

Archetypes 是新内容的模板，通常位于 `~/archetypes` 文件夹下，由元数据（frontmatter）和标记内容（markup）组成，元数据可以使用 TOML、YAML、JSON。

`~/archetypes/default.md` 是默认的内容模板，Hugo Narrow 有两个内容模板：

- `archetypes/default.md`：默认模板，用于 `posts` 和其他默认内容。
- `archetypes/projects.md`：项目模板，用于项目文件。

## 创建新文章

使用下面的命令可以使用默认模板创建一个新的文章，文件名为 `my-first-post`：

```bash
hugo new content posts/my-first-post.md
```

## 创建新项目

使用下面的命令可以使用项目内容模板创建一个新的文章，文件名为 `my-first-project`：

```bash
hugo new content projects/my-first-project.md
# 使用 --kind 参数
hugo new content --kind projects projects/my-first-project.md
```

## 自定义内容模板

如果你需要自定义内容模板，可以在站点根目录下的 archetypes 文件夹下创建对应文件: `~/archetypes/default.md`。

Hugo 遵循下面的顺序查找内容模板：

1. `archetypes/posts.md`
2. `themes/hugo-narrow/archetypes/posts.md`
3. `archetypes/default.md`
4. `themes/hugo-narrow/archetypes/default.md`

如果上述模板都不存在，Hugo 会使用内置的默认内容模板。

> [!NOTE]
>
> 访问 [Hugo 文档](https://gohugo.io/content-management/archetypes/) 了解更多。
