---
title: Basic
weight: 41
sidebar:
  open: true
prev: /docs/configurations/
next: /docs/configurations/menus
---

Hugo supports `hugo.toml`、`hugo.yaml`、`hugo.json` format and follow the order, supporting split configuration file by envirament, root configuration key, and language.

> [!NOTE]
> See [Hugo Documentation](https://gohugo.io/configuration/introduction/#configuration-directory) for more details.

Hugo Narrow uses split configuration with `YAML`.

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


The site configuration is not much different from that of a regular Hugo site; the special part is:

1. `permalinks.projects` sets the permalinks for projects.
2. `outputFormats.WebAppManifest` automatically generates the `WebAppManifest` configuration for the theme.
3. `highlight.lineNumbersInTable` needs to be set to `false`.
4. `highlight.style` setting does not take effect. To change the Hugo Narrow codeblock style, you need to modify the CSS files.
5. The minimum required version of Hugo is 0.146.

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
    lineNumbersInTable: false # Set to false
    noClasses: false
    style: github # No need to change
    tabWidth: 2

outputs:
  home: ["HTML", "RSS", "JSON", "WebAppManifest"]

# Custom output
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
