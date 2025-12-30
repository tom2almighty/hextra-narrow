---
title: Narrow v1.2.1
date: 2025-12-26
---

本次更新添加了项目内容和两个短代码：`button` 和 `icon`。

<!--more-->

## 新特性

- 添加目录开关（`params.toc.enabled: true`）。
- 添加自定义 head 模板。
- 添加项目内容。
- 添加 `button` 和 `icon` 短代码。

### Button 短代码

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

### Icon 短代码

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

## Bug 修复

- 移除冗余样式文件。
- 调整链接样式以修复不必要的下划线。
