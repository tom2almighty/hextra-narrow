---
title: Archetypes
weight: 33
sidebar:
  open: true
prev: /docs/content-management/local-resources
next: /docs/content-management/frontmatter
---

Archetypes is template for new content, located at `~/archetypes`. A content file consists of frontmatter and markup. Frontmatter can be TOML, YAML, JSON.

`~/archetypes/default.md` is the default archetype. Hugo Narrow include two archetypes:

- `archetypes/default.md`: default archetype, used for `posts` and others.
- `archetypes/projects.md`: project archetype, used for project files.

## Create a new post

Use the following command to create a new post named `my-first-post` with the default archetype:

```bash
hugo new content posts/my-first-post.md
```

## Create a new project

Use the following command to create a new project named `my-first-project` with the project archetype:

```bash
hugo new content projects/my-first-project.md
# use `--kind` parameter
hugo new content --kind projects projects/my-first-project.md
```

## Custom archetypes

If you need create your own archetype, create a file at the root folder of the site: `~/archetypes/default.md`

Hugo follows the lookup order for archetypes:

1. `archetypes/posts.md`
2. `themes/hugo-narrow/archetypes/posts.md`
3. `archetypes/default.md`
4. `themes/hugo-narrow/archetypes/default.md`

If none of these exists, Hugo uses a built-in default archetype.

> [!NOTE]
>
> See [Hugo Documentation](https://gohugo.io/content-management/archetypes/) for more details.
