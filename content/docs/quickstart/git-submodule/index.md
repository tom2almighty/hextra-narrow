---
title: Git Submodule
weight: 22
prev: /docs/quickstart/hugo-mod
next: /docs/content-management
sidebar:
  open: true
---

## Prerequisites

You should install the following softwares before start:

- [Hugo Extended](https://gohugo.io/installation/), Version 0.146 or later
- [Git](https://git-scm.com/)

## Steps

{{% steps %}}

### Init a new site

```bash
hugo new site my-site --format=yaml
```

### Add hugo narrow as a git submodule

```bash
cd my-site
git init
git submodule add https://github.com/tom2almighty/hugo-narrow.git themes/hugo-narrow
```

### Copy example site files

Copy all files of `~/themes/hugo-narrow/exampleSite/` to the root folder of the site.

Make sure the configuration at `~/config/_default/hugo.yaml` is right： `theme: hugo-narrow`.

> [!NOTE]
>
> If you need to modify the theme, copy the theme files you want to modify to the same path in the root directory of your site and define your modifications there.
>
> With this method, you cannot commit modifications to GitHub. If you want to save your modifications to a GitHub repository, you can fork the theme and then replace the submodule added via git submodule with your repository address.

### Localhost preview

```bash
hugo server --buildDrafts --disableFastRender
```

Visit `http://localhost:1313` see your new site.

{{% /steps %}}

## Update theme

To update **ALL** submodule, use the command:

```bash
git submodule update --remote --recursive
```

To update theme submodule, use the command:

```bash
git submodule update --remote --recursive themes/hugo-narrow
```

> [!NOTE]
>
> See [Git Submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules) for more details.
