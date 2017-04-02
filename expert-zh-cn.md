---
title: 进阶设定
version: 1.3.2
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

从 `1.3.0` 版本开始，您可以使用 `hexo-prism-plugin` 进行代码染色，具体文档请参阅[Hexo-Prism-Plugin 插件文档](https://github.com/ele828/hexo-prism-plugin)