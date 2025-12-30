---
title: Extended Shortcodes
weight: 72
sidebar:
  open: true
prev: /docs/shortcodes/build-in-shortcodes
next: /docs/advanced/
---

Delete the `\` between `{{` and `}}`.

## Bilibili

```bash
{\{< bilibili VIDEO_ID PART_NUMBER >}\}
```

Support AV number or BV number, `PART_NUMBER` is optinal, specifies which part to display when provided.

## Tencent Video

```bash
{\{< tencent VIDEO_ID >}\}
```

## Masonry Gallery

```bash
{\{< masonry columns=4 gutter=15 >}\}
![Image 1](image1.jpg)
![Image 2](image2.jpg)
{\{< /masonry >}\}
```

## Link cards

Link cards support three methods to import.

### Use parameters directly

```bash
{\{< link title="Google" description="The world largest search engine." url="https://google.com" icon="https://google.com/favicon.ico" >}\}
```

### Use id or ref paremeter

List data at `data/links.yaml`, then use `id` or `ref` parameter:

```bash
{\{< link id="github" >}\}
{\{< link ref="github" >}\}
```

```yaml {filename="data/links.yaml"}
social:
  - id: github
    title: GitHub
    description: The world's largest code hosting platform.
    url: https://github.com
    icon: https://github.com/fluidicon.png

  - id: linkedin
    title: LinkedIn
    description: Career Social Network.
    url: https://linkedin.com

tool:
  - id: vercel
    title: Vercel
    description: Deploy and Development Platform.
    url: https://vercel.com
    icon: https://vercel.com/favicon.ico
  
  - id: netlify
    title: Netlify
    description: Deploy and Development Platform.
    url: https://netlify.com
    icon: https://netlify.com/favicon.ico

  - id: github-pages
    title: GitHub Pages
    description: Static Pages Hosting.
    url: https://pages.github.com
    icon: https://github.com/fluidicon.png

```

### Use group or category parameter

List data at `data/links.yaml`, then use `group` or `category` parameter:

```bash
{\{< link group="social" >}\}
{\{< link category="social" >}\}
```

> [!NOTE]
> `icon` paramater is not required, if you don't define the value, the partials will find the favicon file(`.svg/.ico`), if still find no avaliable icons, it will fallback to `link.svg` of assets folder.

## Button

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

## Icon

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

## Custom shortcodes

Add your shortcode templates in the `~/layout/_shortcodes` directory. If using Tailwind CSS, you'll need to compile styles locally to apply them to the theme.
