---
title: Narrow v1.1.0
date: 2025-06-17
---


This release refactor the configuration of gallery, add a shortcode of masonry gallery.

<!--more-->

## Breaking Changes

Gallery configuration structure has been updated. Please update your Hugo configuration.

```yaml
params:
  # GLightbox Configuration
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

  # Justified Gallery Configuration  
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

Visit [Release Notes](https://github.com/tom2almighty/hugo-narrow/releases/tag/v1.1.0).

## New Features

- Masonry Gallery Shortcode: Added support for masonry/waterfall layout with the new `{\{< masonry >}}` shortcode

```markdown
{\{< masonry columns=4 gutter=15 >}\}
![Image 1](image1.jpg)
![Image 2](image2.jpg)
{\{< /masonry >}\}
```

## Improvements

- New Lightbox System: Migrated from lightGallery to GLightbox for improved performance and modern user experience
- Enhanced Justified Layout: Replaced jQuery-based justified gallery with flickr-justified-gallery for better native JavaScript support
- Removed jQuery Dependency: Complete elimination of jQuery from the gallery system, resulting in faster loading times and reduced bundle size

## Bug Fixes

- Fixed i18n translation issues in post-meta component
- Resolved analytics template inclusion problem
