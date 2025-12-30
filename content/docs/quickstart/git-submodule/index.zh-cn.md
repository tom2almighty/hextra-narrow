---
title: Git 子模块
weight: 22
prev: /docs/quickstart/hugo-mod
next: /docs/content-management
sidebar:
  open: true
---

## 安装要求

在开始之前，你需要安装以下软件：

- [Hugo 扩展版](https://gohugo.io/installation/) 且版本大于等于 0.146。
- [Git](https://git-scm.com/)

## 步骤

{{% steps %}}

### 初始化新的站点

```bash
hugo new site my-site --format=yaml
```

### 将 Hugo Narrow 添加为 Git 子模块

```bash
cd my-site
git init
git submodule add https://github.com/tom2almighty/hugo-narrow.git themes/hugo-narrow
```

### 复制示例站点配置

将 `~/themes/hugo-narrow/exampleSite/` 下的内容复制到站点根目录下。

确保 `~/config/_default/hugo.yaml` 中主题配置正确： `theme: hugo-narrow`

> [!NOTE]
>
> 如果你需要修改主题，将你想要修改的主题文件复制到站点根目录相同路径，在其中定义你的修改。
>
> 使用这种方式你无法提交修改到 GitHub。如果你希望保存你的修改到 GitHub 仓库，你可以 fork 主题，然后将 git submodule 添加的子模块替换成你的仓库地址。

### 本地预览

```bash
hugo server --buildDrafts --disableFastRender
```

访问 `http://localhost:1313` 查看预览站点。

{{% /steps %}}

## 更新主题

更新仓库**所有**子模块，使用命令：

```bash
git submodule update --remote --recursive
```

更新主题子模块，使用命令：

```bash
git submodule update --remote --recursive themes/hugo-narrow
```

> [!NOTE]
>
> 更多详情参阅 [Git 子模块](https://git-scm.com/book/en/v2/Git-Tools-Submodules)
