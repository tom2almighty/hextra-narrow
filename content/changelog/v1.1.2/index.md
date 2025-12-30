---
title: Narrow v1.1.2
date: 2025-07-02
---

This release optimize the parameters of posts license.

<!--more-->

## Bug Fixes

- Fixed frontmatter license params is not taking effect.

## Style

- Image display center.

## Breaking Changes

- license params add `author` and `show` params
- delete `showLicense` params

```diff
params:
  post:
-   showLicense: true
    license:
+     show: true
+     author: "Hugo Narrow"
      name: "CC BY-NC-SA 4.0"
      description: "This work is licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License. Please attribute the source, use non-commercially, and maintain the same license."
      url: "https://creativecommons.org/licenses/by-nc-sa/4.0/"
      displayName: "CC BY-NC-SA 4.0"

```
