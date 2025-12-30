---
title: Color Schemes
weight: 56
sidebar:
  open: true
prev: /docs/features/dock
next: /docs/features/posts
---

Hugo Narrow build in many color schemes, you can change scheme by the button at header, custom schemes also supported.

```yaml {filename="params.yaml"}
colorScheme: "default"
themes:
  default:
    name: "Default"
    order: 1
  claude:
    name: "Claude"
    order: 2
  bumblebee:
    name: "Bumblebee"
    order: 3
  emerald:
    name: "Emerald"
    order: 4
  nord:
    name: "Nord"
    order: 5
  sunset:
    name: "Sunset"
    order: 6
  abyss:
    name: "Abyss"
    order: 7
  dracula:
    name: "Dracula"
    order: 8
  amethyst:
    name: "Amethyst"
    order: 9
  slate:
    name: "Slate"
    order: 10
  twitter:
    name: "Twitter"
    order: 11
```

## Custom Schemes

If you want to add your scheme, create a css file at `~/assets/css/custom/` directory, then add the new scheme  in `params.themes` in the above, here is the virable sample:

```css
[data-theme="dracula"] {
  --color-primary: oklch(0.70 0.15 346.812);
  --color-primary-foreground: oklch(0.98 0.007 106.545);
  --color-secondary: oklch(0.68 0.12 301.883);
  --color-secondary-foreground: oklch(0.98 0.007 106.545);
  --color-accent: oklch(0.75 0.10 66.558);
  --color-accent-foreground: oklch(0.20 0.024 66.558);
  --color-background: oklch(0.95 0.01 277.508);
  --color-foreground: oklch(0.30 0.022 277.508);
  --color-muted: oklch(0.90 0.015 277.508);
  --color-muted-foreground: oklch(0.50 0.02 277.508);
  --color-border: oklch(0.82 0.02 277.508);
  --color-card: oklch(0.95 0.01 277.508);
  --color-card-foreground: oklch(0.30 0.022 277.508);
  --color-popover: oklch(0.97 0.005 277.508);
  --color-popover-foreground: oklch(0.30 0.022 277.508);

  --color-note: oklch(0.65 0.15 240);
  --color-tip: oklch(0.70 0.14 160);
  --color-important: oklch(0.70 0.15 346.812);
  --color-warning: oklch(0.75 0.16 85);
  --color-caution: oklch(0.65 0.18 15);
}

[data-theme="dracula"].dark {
  --color-primary: oklch(0.755 0.183 346.812);
  --color-primary-foreground: oklch(0.151 0.036 346.812);
  --color-secondary: oklch(0.742 0.148 301.883);
  --color-secondary-foreground: oklch(0.148 0.029 301.883);
  --color-accent: oklch(0.834 0.124 66.558);
  --color-accent-foreground: oklch(0.167 0.024 66.558);
  --color-background: oklch(0.288 0.022 277.508);
  --color-foreground: oklch(0.977 0.007 106.545);
  --color-muted: oklch(0.394 0.032 275.524);
  --color-muted-foreground: oklch(0.879 0.006 275.524);
  --color-border: oklch(0.45 0.035 277.508);
  --color-card: oklch(0.32 0.025 277.508);
  --color-card-foreground: oklch(0.977 0.007 106.545);
  --color-popover: oklch(0.394 0.032 275.524);
  --color-popover-foreground: oklch(0.977 0.007 106.545);

  --color-note: oklch(0.70 0.14 240);
  --color-tip: oklch(0.75 0.13 160);
  --color-important: oklch(0.755 0.183 346.812);
  --color-warning: oklch(0.80 0.15 85);
  --color-caution: oklch(0.70 0.17 15);
}
```

> [!NOTE]
> You can also add new scheme at  `~/assets/css/theme.css` or `~/assets/css/custom.css`.
>
> Dependencies are required: `pnpm add -D tailwindcss @tailwindcss/cli`
>
> Run the compile command: `npx tailwindcss -i ./assets/css/main.css -o ./assets/css/compiled.css`
