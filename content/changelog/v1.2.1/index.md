---
title: Narrow v1.2.1
date: 2025-12-26
---

This release add a new content type for projects and two shortcodes `button`, `icon`.

<!--more-->

## Features

- Add toggleable Table of Contents (enable via `params.toc.enabled: true`)
- Support custom head partials
- Add projects content support
- button & icon shortcodes

### Button Shortcodes

```markdown
{\{< button text="Learn More" url="/about" >}\}
{\{< button text="GitHub" url="https://github.com" icon="github" target="_self" >}\}
{\{< button text="Download" url="/download" variant="outline" size="lg" >}\}
```

**Parameters:**

- `text`: Button text (required, or use inner content)
- `url`: Link address (required)
- `variant`: `primary`, `secondary`, `outline` (default: primary)
- `size`: `sm`, `md`, `lg` (default: `md`)
- `icon`: Theme icon name
- `target`: `_blank`, `_self` (default: `_blank`)
- `rel`: Link relationship (noopener noreferrer is automatically added when `_blank` is used)

### Icon Shortcodes

Display SVG icons from the `~/assets/icons/` directory:

```markdown
{\{< icon name="heart" >}\}
{\{< icon name="github" size="lg" >}\}
{\{< icon name="sun" class="text-primary" >}\}
```

**Parameters:**

- `name`: Icon name (required) - Check `assets/icons/` for available icons or place custom icons in this directory, or place the custom icon in this directory
- `size`: `xs`, `sm`, `md`, `lg`, `xl`, `2xl` (default: `md`)
- `class`: Custom CSS class, which can be used to change colors

## Bug Fixes

- Remove redundant style files
- Adjust link class to fix unwanted element underlines
