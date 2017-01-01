---
title: 主题介绍
version:
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
Scheme 的切换通过更改 **主题配置文**件，搜索 `scheme` 关键字。 你会看到有几行 scheme 的配置，将你需用启用的 scheme 去掉前面注释 `#` 即可。

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

#### uiux

用于设置主题 UI 与 UX。
- slogan: 显示在 `blog_info` 模块中的标语，现在可以设置多行标语（见下方）
- theme_color: 主题主要颜色。大部分地方使用此颜色。
- theme_sub_color: 主题辅助颜色。
- hyperlink_color: 超链接颜色。
- button_color: 按钮颜色，例如 `toTop` 或 `menu_button`。
- android_chrome_color: 安卓 Chrome 浏览器地址栏颜色。
- nprogress_color: 页面加载时顶部加载进度条的颜色。
- nprogress_buffer: 页面加载时顶部加载进度条的缓冲。

多行标语使用
```yaml
  slogan: 
   - "标语第一行"
   - "标语第二行"
   - "标语第三行"
```
即可分行显示

#### js_effect

用来控制 Material 主题中自带的多种 js 特性。
- fade: 页面加载时部分模块的渐显效果。默认为 true。
- smoothscroll: 页面平滑滚动特效。默认为 false。

#### reading

用于设置阅读体验。
- markdown: Markdown 解析样式。目前有三种样式，分别是 `Material`, `Github`, `Plain`。
- entry_excerpt: 首页文章输出摘要的字符长度。默认为80。
- code_highlight: 文章内代码高亮的样式，具体设置详情：[代码高亮样式](/expert/#代码高亮样式)。

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
- upyun_logo: 默认为注释状态。取消注释后显示于 `sidebar` 底部。用于又拍云联盟的使用。
- random_thumbnail: 随机缩略图的路径。

#### fonts

用于设置站点的字体。

默认值为 `Roboto, "Helvetica Neue", Helvetica, "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", "微软雅黑", Arial, sans-serif` 

>该字体设定较为规范，如无特殊要求 无需额外修改。

#### qrcode

用于在文章页中显示二维码，扫描二维码即可直接打开文章。  
需要 hexo-helper-qrcode 支持，使用 `npm install hexo-helper-qrcode --save` 进行安装。


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


#### dropdown
用于设置 Paradox 侧边栏用户下拉菜单，默认为空。
>参考配置样式

>```yaml
dropdown: 
	Email Me: 
		link: "#"
		icon: email
```

#### pages

用于设置独立页面，默认为空。填写条目后独立页面入口将显示在：
- `blog_info` `Page` 按钮的下拉菜单中。(Scheme Paradox)
- 侧边栏 `独立页面` 菜单中。(Scheme Paradox)
- 站点左侧。(Scheme Isolation)

>参考配置样式
```yml
pages:
	友情链接: "/links/"
	时间轴归档: "/timeline/"
```

首个参数为入口名字；后一个参数为相对路径，对应 hexo 目录下的 `source` 文件夹内的相应文件夹。


### Integrated Services

#### comment

用于于设置评论系统。

具体设置参考 [评论系统](/services/#评论系统)

目前可使用 `duoshuo` `disqus`。
- use: 
- shortname: 
- duoshuo_thread_key: 用于设置多说 tread key 的使用，默认为 `path`，可设置为 `id`。
- duoshuo_embed_js_url: 多说 js。

#### search

用于设置搜索系统。

具体设置参考 [搜索系统](/services/#搜索系统)

目前可使用 `google ` `swiftype` `local`。
- use
- swiftype_key


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