---
title: Frontmatter
weight: 34
sidebar:
  open: true
prev: /docs/content-management/archetypes
next: /docs/content-management/markdown
---

Frontmatter is configruation section at the beginning of markdown files, it uses two `---` wrap (different data uses different symbol wrap, YAML is recommended) to define posts' basic information, or cover some parameters in `hugo.yaml`. Every archetypes has common and unique frontmatters.

If you don't know what is archetypes, see [Archetypes](/docs/content-management/archetypes).

## Default Archetypes

Default archetypes is used to generate posts and other content for which no content template is defined.

### Basic

```yaml
---
# required
title: "Post Title"
date: 2025-06-13
# Optinal
description: "Post description"
draft: false
categories: ["categories 1", "categories 2"]
tags: ["tags 1", "tags 2"]
slug: "custom-url"
---
```

If you don't matter SEO, you can use the theme archetypes to auto generate slug, it generates a random 7-digit string.

```yaml
slug: {{ substr .File.UniqueID 0 7 }}
```

> [!NOTE]
>
> See [Hugo Documentation](https://gohugo.io/configuration/front-matter/) for more frontmatter.

### Post Cover

Follow this to set a post cover:

```yaml
cover: ""
```

Hugo Narrow has a fallback for cover:

- `cover` value
- `cover` has no value
  - if `~/data/placeholder_images.yaml` set `enabled: true`, use random cover list.
  - if `~/data/placeholder_images.yaml` set `enabled: false`, automatically generate a placeholder.

#### Fixed

`cover` value support a external link or local resources, local resources follow the lookup order: `Page Resources> Global Resources > Static Resources`。

If you don't know how to import local resources, see [Local Resources](/docs/content-management/local-resources).

#### Random Cover

`cover` value is unset and `~/data/placeholder_images.yaml` set `enabled: true`, you can place a random cover list at `~/data/placeholder_images.yaml`:

```yaml
enabled: true

# Cover URLs (external link or local link)
images:
  # Picsum Photos
  #- "https://picsum.photos/800/600?random=1"
  #- "https://picsum.photos/800/600?random=2"
  #- "https://picsum.photos/800/600?random=3"
  #- "https://picsum.photos/800/600?random=4"
  #- "https://picsum.photos/800/600?random=5"
  #- "https://picsum.photos/800/600?random=6&blur=1"
  #- "https://picsum.photos/800/600?random=7&grayscale"
  # local images
  - "/images/placeholder/1.jpg"
  - "/images/placeholder/2.jpg"
  - "/images/placeholder/3.jpg"  
  - "/images/placeholder/4.jpg"
  - "/images/placeholder/5.jpg"
  - "/images/placeholder/6.jpg"
  - "/images/placeholder/7.jpg"
  - "/images/placeholder/8.jpg"
```

`cover` value is unset and `~/data/placeholder_images.yaml` set `enabled: false`, Hugo Narrow will generate some placeholder whick adapt for color schemes automatically.

### Other frontmatter

Default(Posts) archetypes also support other frontmatters, these configurations involve some features of the theme, usually configured in `hugo.yaml`, but you can also modify the overrides in the frontmatter.

```yaml
# math formula
katex:
  enabled: true
  delimiters:
    - left: $$
      right: $$
      display: true
    - left: $
      right: $
      display: false

# charts
mermaid:
  enabled: true

# related posts
showRelated: true

# posts license
post:
  license:
    show: true
    author: "Hugo Narrow"
    name: "CC BY-NC-SA 4.0"
    description: "This work is licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License. Please attribute the source, use non-commercially, and maintain the same license."
    url: "https://creativecommons.org/licenses/by-nc-sa/4.0/"
    displayName: "CC BY-NC-SA 4.0"

# Glightbox
lightbox:
  enabled: true
  loop: true
  width: 80vw
  height: 80vh
  touchNavigation: true
  draggable: true
  zoomable: true
  preload: true
  descPosition: bottom

# gallery
justified_gallery:
  enabled: true
  rowHeight: 300
  gutter: 30
  lastRow: center
  transitionDuration: 0.3s
  resizeDebounce: 100
  rowHeightTolerance: 0.25
  maxRowsCount: 999999
  calculateItemsHeight: false

```

## Projects Archetype

The projects archetype is used to generate project files. The basic frontmatter parameter are the same as the default archetype. There are also unique frontmatter. The following are the unique parameters of the projects archetype:

```yaml
cover: ""            # same as default archetype
featured: false
github: ""
demo: ""
website: ""
tech_stack:
  - Technology 1
  - Technology 2
status: "completed"  # Options: completed, in_progress, planning

```
