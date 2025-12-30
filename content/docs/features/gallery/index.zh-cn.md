---
title: 图库
weight: 62
sidebar:
  open: true
prev: /docs/features/codeblock
next: /docs/features/miscellaneous
---

Hugo Narrow 支持图片点击放大功能，使用 [GLightbox](https://github.com/biati-digital/glightbox) 库创建灯箱，同时支持 `justified` 布局和 `Masonry` 布局。`justified` 布局使用 [lickr-justified-gallery](https://github.com/nk-o/flickr-justified-gallery) 库实现，使用原生 markdown 输入，Masonry 布局使用 [Macy.js](https://github.com/bigbite/macy.js) 库实现，使用短代码输入。

> [!TIP]
> 图库相关参数可以在文章 frontmatter 覆盖设置。

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

## Justified 布局图库

直接使用 markdown 方式引入图像资源，每行一个资源链接，中间无空行的图像组视为同一个图库。 下面的示例为两个图库，第一个图库包含两个图像资源，第二个图库包含三个图像资源。

```markdown
![](images/image01.jpg)
![](images/image02.jpg)

![](images/image03.jpg)
![](images/image04.jpg)
![](images/image05.jpg)
```

## Masonry 布局图库

使用短代码实现，访问 [扩展短代码](/docs/shortcodes/extended-shortcodes)。
