---
title: Expert
version:
permalink: en/expert
id: 4
lang: en
---
## Add custom code

If you want to add custom `font-face` or statistical code (such as `Google Analytics`) to your site.

You need to create a folder named `_data` (no rename) in the` source` folder in the hexo directory.

And then create a file called head.yml in the file.

The single code format is:

```yaml
Name:
     "Put your code here"
```

The code will be displayed before `</head>`,
`Name` will appear as a comment above the code.

## Palette

[Color palette](https://material.google.com/style/color.html#color-color-palette)

## Material icons

Custom the icons in Material Theme, such as `dropdown: icon`.

[Material icons](https://material.io/icons/)

## Code highlight

[Preview 77 kinds style](https://highlightjs.org/static/demo/)

At `Theme folder -> source -> css -> highlight` directory has all of the stylesheet，fill in the corresponding name.

For example：
```yml
reading:
    code_highlight: solarized-dark
```