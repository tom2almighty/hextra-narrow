---
title: Header
weight: 54
sidebar:
  open: true
prev: /docs/features/author
next: /docs/features/dock
---


Hugo Narrow supports set sticky header, logo, theme switch, dark mode switch, language switch.  

1. logo placed at `~/static` directory, leave empty to use site title first letter.
2. Language switch mode is supported which is click to switch(cycle) or click to show panel(dropdown).

```yaml {filename="params.yaml"}
header:
  sticky: true 
  logo:
    image: "/images/logo.svg"  # Logo path relative to static folder, leave empty to use site title first letter
    link: "/"  # Click to home page
  # UI Components Control (header controls)
  showThemeSwitch: true      # Set to false to hide theme style switcher (palette icon)
  showDarkModeSwitch: true   # Set to false to hide dark mode switcher (sun/moon icon)
  showLanguageSwitch: true   # Set to false to hide language switcher
  languageSwitchMode: "dropdown"  # Language switch mode: "dropdown" (show panel) or "cycle" (direct cycle)
```
