---
title: Gallery
weight: 62
sidebar:
  open: true
prev: /docs/features/codeblock
next: /docs/features/miscellaneous
---

Hugo Narrow supports lightbox, use [GLightbox](https://github.com/biati-digital/glightbox). Also justified gallery, use [lickr-justified-gallery](https://github.com/nk-o/flickr-justified-gallery), writing by markdown.Masonry gallery use [Macy.js](https://github.com/bigbite/macy.js), writting by shortcode.

> [!TIP]
> The parameters of gallery can be coverd by posts frontmatter.

```yaml {filename="params.yaml"}
# GLightbox
lightbox:
  enabled: false
  loop: true
  width: 80vw
  height: 80vh
  touchNavigation: true
  draggable: true
  zoomable: true
  preload: true
  descPosition: bottom

# Justified Gallery
justified_gallery:
  enabled: false
  rowHeight: 300
  gutter: 30
  lastRow: center
  transitionDuration: 0.3s
  resizeDebounce: 100
  rowHeightTolerance: 0.25
  maxRowsCount: 999999
  calculateItemsHeight: false
```

## Justified Gallery

Directly import image resources using markdown syntax, with one resource link per line. Image groups without empty lines between them are considered as one gallery.
The example below shows two galleries, the first containing two image resources, and the second containing three image resources.

```markdown
![](images/image01.jpg)
![](images/image02.jpg)

![](images/image03.jpg)
![](images/image04.jpg)
![](images/image05.jpg)
```

## Masonry Gallery

Masonry gallery use shortcode, see [Extended Shortcodes](/docs/shortcodes/extended-shortcodes) for more details.
