---
title: 基础配置
weight: 41
sidebar:
  open: true
prev: /docs/configurations/
next: /docs/configurations/menus
---

Hugo 配置文件格式支持：`hugo.toml`、`hugo.yaml`、`hugo.json`，并按照上述顺序索引，支持根据环境、根配置键、语言拆分单个配置文件。

> [!NOTE]
> 访问 [Hugo 文档](https://gohugo.io/configuration/introduction/#configuration-directory) 查看详细内容。

Hugo Narrow 使用拆分的配置结构，格式采用 `YAML`。

{{< filetree/container >}}
  {{< filetree/folder name="exampleSite" >}}
    {{< filetree/folder name="config" >}}
      {{< filetree/folder name="_default" >}}
        {{< filetree/file name="hugo.yaml" >}}
        {{< filetree/file name="languages.yaml" >}}
        {{< filetree/file name="menus.yaml" >}}
        {{< filetree/file name="params.yaml" >}}
      {{< /filetree/folder >}}
    {{< /filetree/folder >}}
    {{< filetree/folder name="content" >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}


站点配置和一般 Hugo 站点差别不大，较为特殊的是：

1. `permalinks.projects` 为项目永久链接设置
2. `outputFormats.WebAppManifest` 为主题自动生成 `WebAppManifest` 配置
3. `highlight.lineNumbersInTable` 需要设置为 `false`
4. `highlight.style` 设置不生效，Hugo Narrow 代码块主题更改需更改样式文件。 
5. Hugo 最低版本为 0.146

```yaml
baseURL: https://hugo-narrow.vercel.app/
languageCode: en-US
defaultContentLanguage: en
defaultContentLanguageInSubdir: false
title: Hugo Narrow
theme: "hugo-narrow"

hasCJKLanguage: true
enableEmoji: true

permalinks:
  posts: /posts/:slug/
  projects: /projects/:slug/
  pages: /:slug/


pagination:
  pagerSize: 6
  path: "page"


taxonomies:
  category: categories
  tag: tags

markup:
  tableOfContents:
    startLevel: 2
    endLevel: 4
    ordered: false
  goldmark:
    renderer:
      unsafe: true
    extensions:
      extras:
        delete:
          enable: true
        insert:
          enable: true
        mark:
          enable: true
        subscript:
          enable: false
        superscript:
          enable: false   
      strikethrough: false 
  highlight:
    codeFences: true
    guessSyntax: false
    lineNos: false
    lineNumbersInTable: false # 设置为 false
    noClasses: false
    style: github # 不需要更改
    tabWidth: 2

outputs:
  home: ["HTML", "RSS", "JSON", "WebAppManifest"]

# 自定义输出格式
outputFormats:
  WebAppManifest:
    mediaType: "application/manifest+json"
    baseName: "site"
    isPlainText: true

module:
  hugoVersion:
    extended: true
    min: 0.146.0
```
