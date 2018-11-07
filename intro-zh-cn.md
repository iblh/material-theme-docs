---
title: 配置介绍
version: 1.4.0
permalink: intro
id: 2
lang: zh-cn
---

这里，我们将介绍主题的基本配置教程，包括 `Site Information`、`Style Settings`、`Menu Settings` 三个部分。

## Site Information

### head

用于配置生成的 HTML 文件的头部信息。

- `favicon`: 网站的 favicon
- `high_res_favicon`: 高清 favicon
- `apple_touch_icon`: iOS 主屏按钮图标
- `keywords`: 网站关键词
- `site_verification`: 搜索引擎验证
  - `google`: 谷歌 Search Console 验证
  - `baidu`: 百度站长平台验证

> 向搜索引擎验证你对站点的所有权，用于向搜索引擎提交 sitemap 和管理站点被搜索引擎收录的情况
> 1. 登录搜索引擎后台，选择使用 `HTML 标记` 验证站点所有权，搜索引擎后台会给你一串类似于这样的东西：
```html
<meta name="xxxx-site-verification" content="xxxxxxxxxxxxxxxxxxxxxxxxxxxx" />
```
> 2. 将 `xxxxxxxxxxxxxxxxxxxxxxxxxxxx` 字符串复制出来，填入对应搜索引擎的设置中，博客更新以后即可通过验证。
> 注：如果你使用了[集成服务](https://material.viosey.com/services/#Google-分析)中的[Google分析](https://analytics.google.com/)服务，那么在配置[谷歌 Search Console](https://www.google.com/webmasters/tools/) 时，可以直接使用Google分析来进行验证，无需再次使用Html标记验证。

- `structured_data`: 启用后会在页面的 head 中生成结构化数据，有助于改善 Google 等搜索引擎的 SEO。这项功能需要你完善地配置主题的 **`站点配置文件`** 和 **`主题配置文件`**，所以如果你在 `hexo g` 中出现问题，尝试禁用该选项。默认值为 true.

### url

用于设置跳转链接。

- rss: 设置生成的 rss 或 atom url
- daily_pic: 设置 `daily_pic` 模块 点击时跳转的 url
- logo: 设置 logo 点击时跳转的 url

> 如何使用 RSS，请访问文档的[集成服务](/service/)，获取启用 RSS 的方法。

## Style Settings

### scheme

Material 主题提供了多种分支主题外观，亦称「Scheme」。
目前 Material 内置三种 Scheme：

#### Nexus（开发中）
最为标准的 Material Design 样式。

#### Paradox

默认 Scheme，是 Material 的最初样式。居中布局，图文并茂。

#### Isolation

Paradox 的至简样式，简洁明了。

----

Scheme 的切换通过更改 **主题配置文件**，搜索 `scheme` 关键字。 你会看到有几行 scheme 的配置，将你需用启用的 scheme 去掉前面注释 `#` 即可。

> 例如 - 选择 Paradox Scheme  

```yaml
#scheme: Nexus
scheme: Paradox
#scheme: Isolation
```

### uiux

用于设置主题 UI 与 UX。

- slogan: 显示在 `blog_info` 模块中的标语，你可以设置单行标语或者多行标语：

> 单行标语使用  

```yaml
  slogan: 标语（支持 HTML 标签）
```

> 多行标语使用  

```yaml
  slogan:
   - "标语第一行"
   - "标语第二行"
   - "标语第三行"
```

- theme_color: 主题主要颜色。主题的大部分地方使用此颜色。
- theme_sub_color: 主题辅助颜色。
- hyperlink_color: 超链接颜色。
- button_color: 按钮颜色，例如 `toTop` 或 `menu_button`。
- android_chrome_color: 安卓 Chrome 浏览器的地址栏颜色。
- nprogress_color: 页面加载时顶部加载进度条的颜色。
- nprogress_buffer: 页面加载时顶部加载进度条的缓冲时间。

> [Color palette](https://material.google.com/style/color.html#color-color-palette)
> 符合 Material Design 的规范颜色。

### js_effect

用来控制 Material 主题中自带的多种 js 特性。

- fade: 页面加载时部分模块的渐显效果，默认为 true。
- smoothscroll: 页面平滑滚动特效，默认为 false。

### reading

用于设置阅读体验。

- entry_excerpt: 首页文章输出摘要的字符长度。默认为 80。

> 注意，这里设定的字符长度包括 `Front-Matter` 的长度，但是在首页，`Front-Matter` 不会显示出来。

### thumbnail

用于设置文章缩略图相关。

- purecolor: 填入颜色代码。如果文章内无设置缩略图，此项又不为空，则使用纯色缩略图。
- random_amount: 随机图片数量，根据 `主题所在文件夹/source/img/random` 中的图片数量设置。Material 主题默认提供了 19 张 Material 风格的缩略图。

### background

用于设置站点背景。

- purecolor: 填入颜色代码。则站点使用纯色背景。
- bgimg: 背景地址，默认调用 `主题文件夹 -> source -> img` 中的 `bg.png`。可更换此图片或者自己填入 url。
- bing: 用于启用“必应美图”的图片作为背景。
    - `parameter`:
        - `color=`: black, blue, brown, green, multi, orange, pink, purple, red, white, yellow.
        - `type=`: A (动物), C (人文), N (自然), S (太空), T (旅行).

### img

用于设置站点图片。

- logo: 显示于 `blog_info` 模块中。
- avatar: 你的头像设置。
- daily_pic: 显示于 `daily_pic` 模块中。
- sidebar_header: 显示于 `sidebar` 顶部。
- footerico: 设置 `footer` 中 SNS 图标的路径。
- random_thumbnail: 随机缩略图的路径。
- footer_image: 你可以在侧边栏底部放置任何你想要的图片。

以又拍云联盟图标为例，你可以这样配置：

```yaml
footer_image:
    upyun_logo:
        link: "https://www.upyun.com/"
        src: "/img/upyun_logo.svg"
```

### fonts

- `family`: 用于设置站点的字体。

> `fonts.family` 默认值为 `Roboto, "Helvetica Neue", Helvetica, "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", "微软雅黑", Arial, sans-serif`
> 该字体设定为 Material Design 的规范，如无特殊要求 无需额外修改。
> 当你修改字体时，请在 `head.yml` 内使用 `<link>` 标签引用你的字体源。如何使用 `head.yml`，请访问[进阶设定](/expert/)中关于 自定义代码 的部分。

- `use`: 用于设置站点字体的引用方式。Material 主题内置了以下三种字体库支持。除此以外，你也可以手动设定你喜欢的谷歌字体反代服务。
  - `google`: 使用 Google 字体库加载 `Roboto` 字体和 `Material Icon`
  - `ustc`: 使用中科大反代的 Google 字体库加载 `Roboto` 字体和 `Material Icon`
  - `baomitu`: 使用 360 前端团队 奇舞团 维护的字体库加载 `Roboto` 字体和 `Material Icon`
  - `custom`, 使用你喜欢的谷歌字体镜像服务加载 `Roboto` 字体和 `Material Icon`。使用该选项需要在 `custom_font_host` 中填入字体库的 URL

> **注意！`custom_font_host` 中设定的字体库的 URL 需要带 proctol（如 https://）且末尾不能带 `/` ！**

### card_elevation

用来设置主题卡片阴影。

### copyright_since

用于设置站点成立的时间。

> 例如，如果你设置了 2015，那么 footer 就会显示 `© 2015 - 2017`。

如果这个值为空，那么 footer 只会显示现在的年份。

### footer text

你可以在页面的 Footer 指定你想显示的文字，支持 HTML 标签；默认为空。
比如，备案号可以这样设定：

```yml
footer_text: '<a href="http://www.miitbeian.gov.cn" rel="nofollow">某ICP备xxxxxxxx号-x</a>'
```

### Code

使用 `Google Prettify` 实现代码高亮。
启用之前你需要禁用 Hexo 自带的代码高亮。

```yml
prettify:
    enable: false # Available value: true | false,
    theme: "vibrant-ink" # default value: "vibrant-ink"   # theme-name without '.css'
```

### Post License

你可以在每篇文章的结尾添加你的版权说明，支持 HTML 标签。License 以粗体显示，默认为空。
比如，你可这样设定 CC License。

```yml
license: 'This blog is under a <a href="/creativecommons.html" target="_blank">CC BY-NC-SA 3.0 Unported License</a>'
```
> 你也可以在页面的 Front-Matter 中为不同文章添加不同的 License。

### Qrcode

用于在文章页中显示二维码，扫描二维码即可直接打开文章。

- enable: 是否显示二维码
- use: 设置生成二维码的方式，可选的有：plugin | online

> 当 `use` 设置为 `plugin` 时，你需要安装 `hexo-helper-qrcode` 插件，使用 `npm install hexo-helper-qrcode --save` 安装。
> 当 `use` 设置为 `online` 时，二维码将会由 `pan.baidu.com` 的 API 生成。

## Menu Settings

### toc

是否显示 TOC(Table of Content) 菜单中的行号。

### sns

用于填写你的 SNS 信息，其中 `email` 会显示在侧边栏，其他信息会以按钮的形式显示在 `footer`。

- email
- twitter
- facebook
- googleplus
- weibo
- instagram
- tumblr
- github
- linkedin
- facebook

### sns_share

用于定义分享菜单中的项目， `false` 的项将不会显示在分享菜单中。

- twitter
- googleplus
- weibo
- linkedin
- qq
- telegram

### dropdown
用于设置 Paradox 侧边栏用户下拉菜单，默认为空。

>参考配置样式

>```yaml
dropdown:
	Email Me:
		link: "mailto: someone@example.com"
		icon: email
```
### homepage

设置 “主页” 按钮

```yaml
use: 设置 true 时会在侧边栏显示 “主页” 按钮.
icon: 在 “主页” 前面显示一个 Material 图标。为空和被注释时则不显示.
divider: 设置成 true
archives
```

### archives

用来设置归档下拉菜单。

```yaml
use: 设置成 true 时在侧边栏显示归档。
icon: 为归档添加一个 Material Icon，注释掉或为空则不显示 Icon
divider: 设置成 true 后会在归档按钮底部增加一条分割线。
```

### categories

用来设置分类显示按钮。

```yaml
use: 设为 true 在侧边栏显示分类按钮。
icon: 在分类按钮前显示一个 Material Icon，注释掉或为空则不显示 Icon
divider: 设置成 true 后会在归档按钮底部增加一条分割线。
```

### pages

用于设置独立页面的入口，默认为空。填写条目后独立页面入口将显示在：

- `logo card` 的 `Page` 按钮下拉菜单中。(Scheme Paradox)
- 侧边栏。(Scheme Paradox)
- 站点左侧。(Scheme Isolation)

请按照如下样例添加个人独立页面。 

```yaml
pages:
    About:
        link: "#about"
        icon: person
        divider: false
```

作为一个单位。

- Name 是该独立页面的名称，请自行修改。
- link 的参数为相对路径，对应 hexo 目录下的 `source` 文件夹内的相应文件夹。
- icon 的参数为自定义的 Material 图标，可用图标可在 [Material icons](https://material.io/icons/) 查询。
- divider 设置成 true 后会在该条目底部增加一条分割线

### article_num

在主题的侧边栏显示文章总数。

```yaml
use: 设置成 true 时会在侧边栏显示文章总数。
divider: 设置成 true 后会在该条目底部增加一条分割线。
```

### footer

配置侧边栏的底部

```yaml
divider: 设置成 true 后会在侧边栏底部之前增加一条分割线。
theme: 设置成 true 后会在侧边栏底部增加一个指向 Material 主题的链接。
```

## Integrated Services
请参考 [集成服务](/services/)
