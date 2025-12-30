---
title: 自定义主题
weight: 101
sidebar:
  open: true
prev: /docs/advanced/
next: 
---

## Git 子模块引入主题

当你使用 `git submodule` 方式添加主题时，将你想要修改的主题文件复制到站点根目录相同路径，在其中定义你的修改。

使用这种方式你**无法**提交修改到 GitHub。

如果你希望保存你的修改到 GitHub 仓库，你可以 fork 主题，然后将 `git submodule` 添加的子模块替换成你的仓库地址。

## Hugo 子模块引入主题

当你使用 Hugo 子模块添加主题时，在 `~/themes` 目录下不会生成文件，因此你需要到主题仓库地址找到需要修改的文件，将其复制到站点根目录相同路径，在其中定义你的修改。

## 自定义 Head

在 `~/layouts/_partials/layout/head/custom-head.html` 文件中添加你的修改。

## 自定义样式

### 直接使用

在站点 `~/assets/css/custom/` 目录下新建**任意名称**的 `CSS` 文件，在其中写入自定义样式即可。

### 编译使用

1. 首先在站点根目录安装依赖：`pnpm add -D tailwindcss @tailwindcss/cli`。
2. 在 `~/assets/css/custom.css` 中或其他样式文件中修改或添加自定义样式。
3. 编译样式文件：`npx tailwindcss -i ./assets/css/main.css -o ./assets/css/compiled.css`

## 自定义 JS

在站点 `~/assets/js/custom/` 目录下新建**任意名称**的 `JavaScript` 文件，在其中写入自定义脚本即可。
