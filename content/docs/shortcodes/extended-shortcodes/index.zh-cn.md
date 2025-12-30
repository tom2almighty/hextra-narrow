---
title: 扩展短代码
weight: 72
sidebar:
  open: true
prev: /docs/shortcodes/build-in-shortcodes
next: /docs/advanced/
---

使用时删除 `{{` 和 `}}` 中间的 `\`

## Bilibili

```bash
{\{< bilibili VIDEO_ID PART_NUMBER >}\}
```

同时支持 AV 号和 BV 号，其中 `PART_NUMBER` 是可选参数，指定后展示对应分集。

## 腾讯视频

```bash
{\{< tencent VIDEO_ID >}\}
```

## Masonry 图库

```bash
{\{< masonry columns=4 gutter=15 >}\}
![Image 1](image1.jpg)
![Image 2](image2.jpg)
{\{< /masonry >}\}
```

## 链接卡片

链接卡片支持三种方式使用。

### 直接使用参数

```bash
{\{< link title="Google" description="世界上最大的搜索引擎。" url="https://google.com" icon="https://google.com/favicon.ico" >}\}
```

### 使用 id 或 ref 参数

在 `data/links.yaml` 罗列数据后使用 `id` 或 `ref` 参数：

```bash
{\{< link id="github" >}\}
{\{< link ref="github" >}\}
```

```yaml {filename="data/links.yaml"}
social:
  - id: github
    title: GitHub
    description: The world's largest code hosting platform.
    url: https://github.com
    icon: https://github.com/fluidicon.png

  - id: linkedin
    title: LinkedIn
    description: Career Social Network.
    url: https://linkedin.com

tool:
  - id: vercel
    title: Vercel
    description: Deploy and Development Platform.
    url: https://vercel.com
    icon: https://vercel.com/favicon.ico
  
  - id: netlify
    title: Netlify
    description: Deploy and Development Platform.
    url: https://netlify.com
    icon: https://netlify.com/favicon.ico

  - id: github-pages
    title: GitHub Pages
    description: Static Pages Hosting.
    url: https://pages.github.com
    icon: https://github.com/fluidicon.png

```

### 使用 group 或 category 参数

在 `data/links.yaml` 罗列数据后使用 `group` 或 `category` 参数：

```bash
{\{< link group="social" >}\}
{\{< link category="social" >}\}
```

> [!NOTE]
> `icon` 参数不是必须的, 如果未指定值, 模板会寻找链接的 `favicon` 文件(`.svg/.ico`), 如果仍未找到可用的值, 会回退到 `assets` 目录下的 `link.svg` 文件。

## 按钮

```markdown
{\{< button text="Learn More" url="/about" >}\}
{\{< button text="GitHub" url="https://github.com" icon="github" target="_self" >}\}
{\{< button text="Download" url="/download" variant="outline" size="lg" >}\}
```

**参数：**

- `text`：按钮文字（必需，或使用内部内容）。
- `url`：链接地址（必需）。
- `variant`：`primary`、`secondary`、`outline`（默认：`primary`）。
- `size`：`sm`、`md`、`lg`（默认：`md`）。
- `icon`：图标名称。
- `target`：`_blank`、`_self`（默认：`_blank`）。
- `rel`：链接关系（`_blank` 时自动添加 `noopener noreferrer`）。

## 图标

显示 `~/assets/icons/` 目录下的图标：

```markdown
{\{< icon name="heart" >}\}
{\{< icon name="github" size="lg" >}\}
{\{< icon name="sun" class="text-primary" >}\}
```

**参数：**

- `name`: 图标名称（必需）- 查看 `~/assets/icons/` 了解可用图标 或者将自定义图放置在此目录下。
- `size`: `xs`, `sm`, `md`, `lg`, `xl`, `2xl` (默认：`md`)。
- `class`: 自定义类名，可以用来更改颜色。

## 自定义短代码

在 `~/layout/_shortcodes` 目录下添加短代码模板，如果使用 `Tailwind CSS`，需要在本地编译样式应用到主题。
