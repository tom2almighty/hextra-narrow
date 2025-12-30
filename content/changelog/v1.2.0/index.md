---
title: Narrow v1.2.0
date: 2025-12-24
---

This release includes extensive optimizations. it's recommend reviewing and validating your Hugo configuration post-update.

<!--more-->

## Breaking Changes

Some parameter levels have been adjusted and the TOC parameter has been added. The specific parameter changes are as follows:

```diff
- params:
-   logo:
-     image: ""
-     link: ""
-   stickyHeader: true
-   showThemeSwitch: true 
-   showDarkModeSwitch: true
-   showLanguageSwitch: true
-   languageSwitchMode: "dropdown"
+ params:
+   header:
+     sticky: true
+     logo:
+       image: ""
+       link: ""
+     showThemeSwitch: true 
+     showDarkMode: true
+     showLanguageSwitch: true
+     languageSwitchMode: "dropdown"
+   toc:
+     position: left # left | right | card
+     maxWidth: "280px"
+     maxHeight: "80vh"
```

## New Features

- Supports sidebar table of contents (TOC).
- Initialize go.mod to support importing the theme via Hugo mod
- Support custom order for homepage sections

## Refactors

- Split the example site configuration
- Adjust the parameter hierarchy of the header

## Bug Fixes

- Icon templates now support solid icons without affecting references in the configuration file
- Adjust some style class names
