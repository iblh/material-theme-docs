---
title: Expert
version: 1.3.0
permalink: en/expert
id: 4
lang: en
---

## Add custom code

If you want to add custom code, like `font-face` or statistical code (such as `Google Analytics`) to your site, you need to create a folder named `_data` (no rename) in the `source` folder in your site directory.

Then create a file called `head.yml` in the file:

```yaml
Name:
    "Put your code here"
```

The code will be displayed before `</head>` tag. `Name` will appear as a comment above the code.

## Palette

See [color palette](https://material.google.com/style/color.html#color-color-palette).

## Material icons

The list of icon used to customized the dropdown or page buttons is available [here](https://material.io/icons/).

## Code highlight

From `Version 1.3.0`, you can use `hexo-prism-plugin` to highlight your codes, visit [Hexo-Prism-Plugin Github](https://github.com/ele828/hexo-prism-plugin) to learn more.