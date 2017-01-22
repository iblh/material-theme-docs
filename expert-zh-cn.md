---
title: 进阶设定
version: 1.2.6
permalink: expert
id: 4
lang: zh-cn
---
## 添加自定义代码
如果想要在站点添加自定义 `font-face` 或者统计代码（例如 `Google Analytics`）。

需要在 hexo 目录下的 `source` 文件夹内创建一个名为 `_data`（禁止改名）的文件夹。

然后在文件内创建一个名为 head.yml 的文件。

单个代码格式为：
```yml
Name:
	"put your code here"
```

代码将显示在 `</head>` 之前，
`Name` 将作为注释显示在代码上方。


## 调色板

[Color palette](https://material.google.com/style/color.html#color-color-palette)

## Material 图标

用于自定义例如 `dropdown: icon` 的图标。

[Material icons](https://material.io/icons/)

## 代码高亮样式

[77 种样式预览](https://highlightjs.org/static/demo/)

在 `主题文件夹 -> source -> css -> highlight` 目录可查看所有样式文件，填入对应文件名即可使用。

例如：
```yml
reading:
	code_highlight: solarized-dark
```