---
title: 主题介绍
version: 1.3.0
permalink: intro
id: 2
lang: zh-cn
---
## 分支「Scheme」介绍

Material 主题提供了多种分支主题外观，亦称「Scheme」。
目前 Material 支持三种 Scheme：
### Nexus（开发中）
最为标准的 Material Design 样式。

### Paradox
默认 Scheme，是 Material 的最初样式。居中布局，图文并茂。

### Isolation
Paradox 的至简样式，简洁明了。

### 切换
Scheme 的切换通过更改 **主题配置文件**，搜索 `scheme` 关键字。 你会看到有几行 scheme 的配置，将你需用启用的 scheme 去掉前面注释 `#` 即可。

>例如 - 选择 Paradox Scheme

>```yaml
#scheme: Nexus
scheme: Paradox
#scheme: Isolation
```


## 主题配置文件介绍

### Site Information

#### head

用于配置生成的 HTML 文件的头部信息。
- favicon
- high_res_favicon: 高清 favicon
- high_res_favicon: iOS 主屏按钮图标
- keywords: 网站关键词

#### url

用于设置跳转链接。
- rss: 设置生成的 rss 或 atom url。
- daily_pic: 设置 `daily_pic` 模块 跳转 url。
- logo: 设置 logo 的跳转 url。


### Style

#### scheme

如果要使用其中一个主题，将前面的注释 `#` 去掉即可。

比如，选择使用 Paradox Scheme，只需要这样配置：

```yaml
#scheme: Nexus
scheme: Paradox
#scheme: Isolation
```

#### uiux

用于设置主题 UI 与 UX。
- slogan: 显示在 `blog_info` 模块中的标语，现在可以设置多行标语：

> 单行标语使用

> ```yaml
  slogan: 标语
```

> 多行标语使用
> ```yaml
  slogan:
   - "标语第一行"
   - "标语第二行"
   - "标语第三行"
```

- theme_color: 主题主要颜色。大部分地方使用此颜色。
- theme_sub_color: 主题辅助颜色。
- hyperlink_color: 超链接颜色。
- button_color: 按钮颜色，例如 `toTop` 或 `menu_button`。
- android_chrome_color: 安卓 Chrome 浏览器地址栏颜色。
- nprogress_color: 页面加载时顶部加载进度条的颜色。
- nprogress_buffer: 页面加载时顶部加载进度条的缓冲。

#### js_effect

用来控制 Material 主题中自带的多种 js 特性。
- fade: 页面加载时部分模块的渐显效果。默认为 true。
- smoothscroll: 页面平滑滚动特效。默认为 false。

#### reading

用于设置阅读体验。

- entry_excerpt: 首页文章输出摘要的字符长度。默认为80。

#### thumbnail

用于设置文章缩略图相关。
- purecolor: 填入颜色代码。如果文章内无设置缩略图，此项又不为空，则使用纯色缩略图。
- random_amount: 随机图片数量，根据 `主题文件夹 -> source -> img -> random` 中的图片数量设置。

#### background

用于设置站点背景。
- purecolor: 填入颜色代码。则站点使用纯色背景。
- bgimg: 背景地址，默认调用 `主题文件夹 -> source -> img` 中的 `bg.png`。可更换此图片或者自己填入 url。
- bing: 用于启用 bing 图片。
  - `parameter` 参数可用：`new`, `color=`, `type=`。
  - `color=`: black, blue, brown, green, multi, orange, pink, purple, red, white, yellow。
  - `type=`: A (animal), C (culture), N (nature), S (space), T (travel)。

#### img

用于设置站点图片。
- logo: 显示于 `blog_info` 模块中。
- avatar: 你的头像设置。
- daily_pic: 显示于 `daily_pic` 模块中。
- sidebar_header: 显示于 `sidebar` 顶部。
- footerico: 设置 `footer` 中 SNS 图标的路径。
- random_thumbnail: 随机缩略图的路径。
- footer_image: 你可以在侧边栏底部放置任何你想要的图片。

比如，你可以这样配置 又拍云 Logo：

```yaml
footer_image:
    upyun_logo:
        link: "https://www.upyun.com/"
        src: "/img/upyun_logo.png"
```


#### fonts

用于设置站点的字体。

默认值为 `Roboto, "Helvetica Neue", Helvetica, "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", "微软雅黑", Arial, sans-serif`

>该字体设定较为规范，如无特殊要求 无需额外修改。

#### card_elevation

用于设置文章列表的卡片阴影，如无特殊要求 无需额外修改。

### Menu

#### sns

用于填写你的 SNS 信息，除了 `email`，其他信息会以按钮的形式显示在 `footer`。

- email: 显示在侧边栏中。
- twitter
- facebook
- googleplus
- weibo
- instagram
- tumblr
- github
- linkedin
- facebook

#### sns_share

用于定义分享菜单中的项目， `false` 的项将不会显示在分享菜单中。

- twitter
- googleplus
- weibo
- linkedin
- qq
- telegram

#### dropdown
用于设置 Paradox 侧边栏用户下拉菜单，默认为空。

以

```
Name:
	link: "/link/"
	icon: icon
```

作为一个单位。

`Name` 是该独立页面的名称，请自行修改。
`link` 的参数为相对路径，对应 hexo 目录下的 `source` 文件夹内的相应文件夹。
`icon` 的参数为自定义的 Material 图标，可用图标可在 [Material icons](https://material.io/icons/) 查询。

>参考配置样式

```yaml
dropdown:
    Email Me:
        link: "#"
        icon: email
```

##### homepage

设置 “主页” 按钮

- `use`: 设置 `true` 时会在侧边栏显示 “主页” 按钮.
- `icon`: 在 “主页” 前面显示一个 Material 图标。为空和被注释时则不显示.
- `divider`: 设置成 `true` 

##### archives

用来设置归档下拉菜单。

- `use`: 设置成 `true` 时在侧边栏显示归档。
- `icon`: 为归档添加一个 Material Icon，注释掉或为空则不显示 Icon
- `divider`: 设置成 `true` 后会在归档按钮底部增加一条分割线。

##### categories

用来设置分类显示按钮。

- `use`: 设为 `true` 在侧边栏显示分类按钮。
- `icon`: 在分类按钮前显示一个 Material Icon，注释掉或为空则不显示 Icon
- `divider`: 设置成 `true` 后会在归档按钮底部增加一条分割线。

##### pages

用于设置独立页面，默认为空。填写条目后独立页面入口将显示在：
- `logo card` `Page` 按钮的下拉菜单中。(Scheme Paradox)
- 侧边栏中。(Scheme Paradox)
- 站点左侧。(Scheme Isolation)


请按照如下样例添加个人独立页面。 `divider` 设置成 `true` 后会在该条目底部增加一条分割线。

```yaml
pages:
    About:
        link: "#about"
        icon: person
        divider: false
    timeline archive:
        link: "/timeline/"
        icon:
        divider: false
```

##### article_num

Used to display the number of articles.

- `use`: 设置成 `true` 时会在侧边栏显示文章总数。
- `divider`: 设置成 `true` 后会在该条目底部增加一条分割线。

##### footer

Used to customize the sidebar footer.

- `divider`: 设置成 `true` 后会在侧边栏底部之前增加一条分割线。
- `theme`: 设置成 `true` 后会在侧边栏底部增加一个指向 Material 主题的链接。

#### qrcode

用于在文章页中显示二维码，扫描二维码即可直接打开文章。  
需要 hexo-helper-qrcode 支持，使用 `npm install hexo-helper-qrcode --save` 进行安装。

#### topPost（开发中）

使用该插件可以将指定文章置顶。
如果您需要这个功能，请使用 `npm install hexo-helper-post-top --save` 安装支持插件，然后将这个开关设置为 `true`。
之后在您需要置顶文章的 `front-matter` 中，添加 `top: true` 即可置顶。

### Integrated Services

#### comment

用于于设置评论系统。

具体设置参考 [评论系统](/services/#评论系统)

目前可使用 `duoshuo` `disqus` 和 `disqus_click`。

> 使用 Disqus_Click 时，页面不会主动加载 Disqus 评论，直到按下按钮。这项设置有助于改善处在 `公开、平等、有序 的中国互联网环境` 下的浏览者体验。

- use:
- shortname:
- duoshuo_thread_key_type: 用于设置多说 tread key 的使用，默认为 `path`，可设置为 `id`。
- duoshuo_embed_js_url: 多说 js。

#### search

用于设置搜索系统。

具体设置参考 [搜索系统](/services/#搜索系统)

目前可使用 `google ` `swiftype` `local`。
- use
- swiftype_key

#### analytics

用于设置访客分析服务，支持 `Google Analysis` 和 `百度站长工具` 

- `baidu_id`: 百度 ID
- `google_id`: Google Analysis 密钥

#### leancloud

具体设置参考 [设置 Leancloud 浏览次数统计](/services/#Leancloud)
- enable: 默认为 false。
- app_id: APP ID。
- app_key: APP Key。
- av_core_mini: 统计 js。

#### busuanzi

具体设置参考 [不蒜子](/services/#不蒜子)
- enable: 默认为 false。
- all_site_uv: 默认为 false。
- post_pv: 默认为 false。
- busuanzi_pure_mini_js: 统计 js。


## 主要协助开发者

[Github - Contributors](https://github.com/viosey/hexo-theme-material/graphs/contributors)

- [pidupuis](https://github.com/pidupuis)
- [neoFelhz](https://github.com/neoFelhz)
- [cubesky](https://github.com/cubesky)
- [AkarinServer](https://github.com/AkarinServer)
- [Halyul](https://github.com/Halyul)
