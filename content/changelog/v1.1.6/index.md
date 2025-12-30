---
title: Narrow v1.1.6
date: 2025-11-16
---

This release add custom content at homepage.

<!--more-->

## New Features

- Homepage author information now supports i18n translation

- Added custom content template between homepage author information and recent posts

```diff
+ params:
+   home_custom:
+   enabled: true
+     files:
+       - custom_1.html
+       - custom_2.html
```

## Bug Fixes

- Fixed incorrect parameter name for clarity in the site configuration file
