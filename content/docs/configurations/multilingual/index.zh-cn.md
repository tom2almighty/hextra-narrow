---
title: 多语言
weight: 43
sidebar:
  open: true
prev: /docs/configurations/menus
next: /docs/features/
---

Hugo Narrow 支持创建多语言站点，在导航栏通过按钮切换显示。

目前 Hugo Narrow 支持如下语言：

- `ar`：阿拉伯语
- `de`：德语
- `en`：英语
- `es`：西班牙语
- `fr`：法语
- `it`：意大利语
- `ja`：日语
- `ko`：韩语
- `pt`：葡萄牙语
- `ru`：俄语
- `vi`：越南语
- `zh-cn`：简体中文
- `zh-tw`：繁体中文

> [!NOTE]
> 翻译使用 AI 完成，如果你需要添加或优化你的语言，欢迎提出 issue 或者 PR。

多语言站点首先需要在站点配置默认语言。

```yaml {filename="hugo.yaml"}
defaultContentLanguage: zh-cn
```

创建翻译配置文件：

```yaml {{filename="languages.yaml"}}
en:
  languageCode: en-US
  languageName: "English"
  weight: 1

zh-cn:
  languageCode: zh-CN
  languageName: "简体中文"
  weight: 2

ja:
  languageCode: ja-JP
  languageName: "日本語"
  weight: 3

fr:
  languageCode: fr-FR
  languageName: "Français"
  weight: 4
```

Hugo 支持两种主要的多语言文件组织方式：**文件名翻译**和**目录翻译**。每种方式都有其优势和适用场景。

## 翻译文件

例如，有一篇文章 `content/posts/my-first-post.md`，可在文件扩展名前指定语言后缀创建 `content/posts/my-first-post.zh-cn.md` 作为中文翻译。

```yaml
content/
├── posts/
│   ├── my-first-post.md
│   ├── my-first-post.zh-cn.md
│   ├── my-first-post.ja.md
│   └── my-first-post.fr.md
├── about/
│   ├── _index.md
│   ├── _index.zh-cn.md
│   ├── _index.ja.md
│   └── _index.fr.md
└── _index.md
```

## 翻译目录

翻译目录需要指定目录位置：

```yaml {filename="languages.yaml"}
languages:
  en:
    contentDir: content/english
    languageName: English
    weight: 10
  zh-CN:
    contentDir: content/zh-CN
    languageName: 简体中文
    weight: 20
```

```yaml
content/
├── en/
│   ├── posts/
│   │   └── my-first-post.md
│   ├── about/
│   │   └── _index.md
│   └── _index.md
├── zh-cn/
│   ├── posts/
│   │   └── my-first-post.md
│   ├── about/
│   │   └── _index.md
│   └── _index.md
├── ja/
│   ├── posts/
│   │   └── my-first-post.md
│   ├── about/
│   │   └── _index.md
│   └── _index.md
└── fr/
    ├── posts/
    │   └── my-first-post.md
    ├── about/
    │   └── _index.md
    └── _index.md
```

> [!NOTE]
> 这种方式目录结构有更多层级，请访问 [Hugo 文档](https://gohugo.io/content-management/multilingual/#translation-by-content-directory) 了解详细内容。
