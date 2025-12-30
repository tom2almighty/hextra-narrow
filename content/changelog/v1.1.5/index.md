---
title: Narrow v1.1.5
date: 2025-09-05
---

This release add dock display mode parameter.

<!--more-->


## New Features

- Open external links in new tabs.
- Support for custom JavaScript files.
- Add a 404 template.
- Add dock display mode parameters.

```diff
params
+  dock: float # Options: "scroll" (show on scroll up), "always" (always visible), "float" (floating)
```

## Style

- Modify the color of superscripts and subscripts
- Adjust the bottom padding of alert blockquotes
