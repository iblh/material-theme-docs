---
title: 进阶设定
version: 1.3.2
permalink: expert
id: 4
lang: zh-cn
---

> 以下部分可能影响到「Material」的正常运作，请务必先了解这些设定背后的相关知识。

-----

## 添加自定义代码

如果想要在站点添加自定义 `font-face` 或者统计代码（例如 `Google Analytics`）。

需要在 hexo 目录下的 `source` 文件夹内创建一个名为 `_data`（禁止改名）的文件夹，并在文件内创建一个名为 head.yml 的文件。

单个代码格式为：

```yml
Name:
	"put your code here"
```

代码将显示在 `</head>` 之前，
`Name` 将作为注释显示在代码上方。

## Material 图标

用于自定义例如 `dropdown: icon` 的图标。

[Material icons](https://material.io/icons/)

## 代码高亮样式

从 `1.3.0` 版本开始，您可以使用 `hexo-prism-plugin` 进行代码染色，具体文档请参阅 [Hexo-Prism-Plugin 插件文档](https://github.com/ele828/hexo-prism-plugin)

## 使用公共 CDN 库

Material 主题从 1.3.2 版本开始支持 [MaterialCDN](/services/#MaterialCDN) 功能，你可以使用自己申请的私有 CDN 加速你的博客。
Material 主题引用了下述第三方库，你可以使用公共 CDN 库加载它们。
使用公共 CDN 的用户需要手动修改主题内的引用 URL。

Material 主题使用的第三方库包括：

###  jQuery 2.2.0

引用于 `/layout/_partial/head.ejs`

### FontAwesome 4.5.0

引用于 `/layout/_partial/config_css.ejs`

### Material Icons 3.0.1

引用于 `/layout/_partial/config_css.ejs`

### nprogress 0.2.0

引用于 `/layout/_widget/nprogress.ejs`

### Mathjax 2.7.0

引用于 `/layout/_widget/mathjax.ejs`

## Disqus_Proxy_Mode

Disqus 由于一些原因，在 **`公开、平等、有序 的 网络审查 地区`** 下的浏览者并不能正常加载 Disqus 评论系统。
为了实现在墙内加载 Disqus 评论的方案，我们在主题里集成了 [disqus-php-api](https://github.com/fooleap/disqus-php-api) 项目。

### 后端配置

你需要一台能正常访问 Disqus 的、支持 PHP 的 WebServer。
在[主题版本发布页面](https://github.com/viosey/hexo-theme-material/releases)下载 `disqus-proxy.zip` ，解压后可得到 `disqus-proxy` 文件夹。

在 `/api/` 目录下找到 `init.php`，配置有关属性。

> 若无评论邮件提醒功能的需求，邮件部分设置项可全部留空。

将 `disqus-proxy` 文件夹上传到你的 WebServer 的目录下。

### 主题配置

在 **主题配置文件** 的 `comment: disqus_proxy_js_url` 中填入你 `disqus-proxy` 目录的 URI。

> **注意！`comment: disqus_proxy_js_url` 中填入的是 `disqus-proxy` 所在目录的 URI，且末尾不需要带 `/` ！**
> 如果你没有修改 `disqus-proxy` 文件夹的文件名，那么你的 URI 应该以 `disqus-proxy` 结尾。
