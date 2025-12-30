---
title: Custom Hugo Narrow
weight: 101
sidebar:
  open: true
prev: /docs/advanced/
next: 
---

## Uses themes by git submodule

When you add the theme using git submodule, copy the theme files you want to modify to the same path in the site's root directory and define your modifications there.

With this method, you **cannot** commit changes to GitHub.

If you want to save your modifications to a GitHub repository, you can fork the theme and then replace the git submodule address with your repository address.

## Uses themes by hugo mod

When you add the theme by hugo mod, it will not generate any files in `~/themes` directory, you need find the files in the github repsitory, copy the files you want to modify to the same path in the site's root directory and define your modifications there.

## Custom Head

Modify in `~/layouts/_partials/layout/head/custom-head.html`.

## Custom style

### Directly

Create `CSS` files with any filename in `~/assets/css/custom/` directory, then modify there.

### Compile

1. Install dependencies in the root directory of the site: `pnpm add -D tailwindcss @tailwindcss/cli`.
2. Create custom style files in `~/assets/css/custom.css` directory.
3. Compiled the style files: `npx tailwindcss -i ./assets/css/main.css -o ./assets/css/compiled.css`.

## Custom JavaScript

Create javascript files with any filename in `~/assets/js/custom/` directory, then modify there.
