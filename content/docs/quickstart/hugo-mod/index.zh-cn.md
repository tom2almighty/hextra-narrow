---
title: Hugo 模块
weight: 21
prev: /docs/quickstart
next: /docs/quickstart/git-submodule
sidebar:
  open: true
---

## 安装要求

在开始之前，你需要安装以下软件：

- [Hugo 扩展版](https://gohugo.io/installation/) 且版本大于等于 0.146。
- [Git](https://git-scm.com/)
- [Go](https://go.dev/)

## 步骤

{{% steps %}}

### 初始化新的站点

```bash
hugo new site my-site --format=yaml
```

### 通过 Hugo 模块引入主题

```bash
# 初始化Hugo模块
cd my-site
hugo mod init github.com/username/my-site

# 添加 Hugo Narrow 主题
hugo mod get github.com/tom2almighty/hugo-narrow
```

### 复制示例站点配置

将 `hugo-narrow/exampleSite/` 下的内容复制到站点根目录下。这种方式在 `~/themes/` 目录下不会创建文件，访问[主题仓库](https://github.com/tom2almighty/hugo-narrow/tree/main/exampleSite)查看文件。

修改 `hugo-narrow/config/_default/hugo.yaml` 配置文件，通过模块引入主题：

```bash
module:
  hugoVersion:
    extended: true
    min: 0.146.0
  imports:
    - path: github.com/tom2almighty/hugo-narrow
```

### 本地预览

```bash
hugo server --buildDrafts --disableFastRender
```

访问 `http://localhost:1313` 查看预览站点。

{{% /steps %}}

## 更新主题

更新仓库中**所有**的模块，使用下面的命令：

```bash
hugo mod get -u
```

更新主题模块使用下面的命令：

```bash
hugo mod get -u github.com/tom2almighty/hugo-narrow
```

> [!NOTE]
>
> 访问 [Hugo 模块](https://gohugo.io/hugo-modules/use-modules/#update-all-modules) 查看 Hugo 模块更新文档。
