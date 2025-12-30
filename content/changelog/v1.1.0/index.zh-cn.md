---
title: Narrow v1.1.0
date: 2025-06-17
---

本次更新重构了图库配置，并添加了瀑布流布局图库短代码。

<!--more-->

## 重大变更

图库配置结构已更新，请及时调整您的 Hugo 配置。

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

详情请参阅 [发布说明](https://github.com/tom2almighty/hugo-narrow/releases/tag/v1.1.0)。

## 功能增强

- 瀑布流图库短代码：新增 `{\{< masonry >}}` 短代码，支持瀑布流布局。

```markdown
{\{< masonry columns=4 gutter=15 >}\}
![Image 1](image1.jpg)
![Image 2](image2.jpg)
{\{< /masonry >}\}
```

## 改进

- 全新灯箱系统：图库灯箱由 lightGallery 迁移至 GLightbox，提升性能与现代化体验。
- 优化分栏布局：jQuery 版 justified gallery 替换为 flickr-justified-gallery，全面支持原生 JavaScript。
- 移除 jQuery 依赖：图库系统完全去除 jQuery，提升加载速度并减小包体积。

## Bug 修复

- 修复 post-meta 组件的 i18n 翻译问题。
- 解决统计模板导入异常问题。
