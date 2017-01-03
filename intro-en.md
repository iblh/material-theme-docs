---
title: Intro
version:
permalink: en/intro
id: 2
lang: en
---
## Branch "Scheme" introduction

Material theme provides a variety of branch theme appearances, also known as "Scheme".
Currently Material supports three schemes:

### Nexus (under development)

The most standard Material Design style.

### Paradox

The default Scheme is the original style of Material. Center layout, illustrated.

### Isolation

Paradox to Jane style, concise and clear.

### Switch

Scheme toggle searches for the `scheme` keyword by changing the ** topic-configuration file. You will see a few lines of the scheme configuration, you need to use the scheme to remove the front comment `#`.

> For example - select Paradox Scheme

> ```yaml
#scheme: Nexus
scheme: Paradox
#scheme: Isolation
```



## Site config file introduction

### Site Information

#### head

Used to configure the generated HTML file header information.

- favicon
- high_res_favicon: HD favicon
- high_res_favicon: iOS Home button icon
  Keywords: site keywords

#### url

Used to set jump links.

- rss: The generated rss or atom url.
- daily_pic: Set `daily_pic` module jump url.
- logo: set the logo's url.

### Style

#### Scheme

If you want to use one of the themes, delete the '#' before the scheme name.

#### uiux

Used to set the theme UI and UX.

- slogan: The slogan displayed in the `blog_info` module, now we support multi line slogan (see below).

> Single line slogan
> ```yaml
  slogan: Slogan
```

> Multi line slogan
> ```yaml
  slogan:
   - "First Line"
   - "Second Line"
   - "Third Line"
```

- theme_color: Theme The main color. Most places use this color.
- theme_sub_color: Theme auxiliary color.
- hyperlink_color: The color of the hyperlink.
- button_color: Button color, such as `toTop` or` menu_button`.
- android_chrome_color: Chrome Chrome address bar color.
- nprogress_color: The color of the top loading progress bar when the page loads.
- nprogress_buffer: The top loading progress bar buffers when the page loads.


We will automatically generate multi line slogan.

#### js_effect

Used to control the Material theme comes with a variety of js features.

- fade: part of the module to load the page fade effect. The default is true.
- smoothscroll: page smooth scrolling effects. The default is false.

#### reading

Used to set the reading experience.

- markdown: Markdown parsing style. There are three styles, `Material`,` Github`, `Plain`.
- entry_excerpt: Home page Outputs the character length of the digest. The default value is 80.
- code_highlight: The style of code field，Specific settings at：[Code highlight](/enl/expert/#Code-highlight)。

#### thumbnail

Used to set up article thumbnail correlation.

- purecolor: Fill in the color code. If no thumbnails are set in the article, and the item is not empty, a solid thumbnail is used.
- random_amount: The number of random pictures, according to the `theme folder -> source -> img -> random` the number of pictures set.

#### background

Used to set the site background.

- purecolor: Fill in the color code. The site uses a solid background.
- bgimg: background address, the default call `theme folder -> source -> img`` bg.png`. You can replace this picture or fill in their own url.
- bing: used to enable bing pictures.
- The `parameter` parameter is available:` new`, `color =`, `type =`.
- `color =`: black, blue, brown, green, multi, orange, pink, purple, red, white, yellow.
- `type =`: A (animal), C (culture), N (nature), S (space), T (travel).

#### img

Used to set the site image.

- logo: Displayed in the `blog_info` module.
- avatar: Your avatar settings.
- daily_pic: Displayed in the `daily_pic` module.
- sidebar_header: Shown at the top of `sidebar`.
- footerico: Sets the path of the SNS icon in `footer`.
- upyun_logo: defaults to the comment state. The annotation is displayed at the bottom of `sidebar`. Used to shoot the use of cloud alliance.
- random_thumbnail: The path of the random thumbnail.

#### fonts

The font used to set the site.

The default values `are Roboto, Helvetica Neue, Helvetica, PingFang SC, Hiragino Sans GB, Microsoft YaHei, Microsoft Yahe, Arial`

> The font settings are more standardized, no special requirements without additional changes.

#### qrcode

Use this to show qrcode in your article.  
Need hexo-helper-qrcode to support this feature. Use "npm install hexo-helper-qrcode --save" to install.  


### Menu

#### sns

Used to fill in your SNS information, in addition to `email`, other information will be displayed in the form of buttons in the` footer`.

- email: Displayed in the sidebar.
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

Used to choose which items will be displayed in share menu.The items with `false`  will not be displayed in the share menu.

- twitter
- googleplus
- weibo
- linkedin
- qq
- telegram


#### dropdown

Used to set the Paradox sidebar user drop-down menu, the default is empty.

> Refer to the configuration style

> ```yaml
> dropdown:
    Email Me:
        link: "#"
        icon: email
```

#### pages

Used to set up a separate page, the default is empty. After the entries are filled in, the separate page entries will appear in:

- `blog_info` drop-down menu. (Scheme Paradox)
- Sidebar (Scheme Paradox)
- The left side of the site. (Scheme Isolation)

> Refer to the configuration style
>
> ```yaml
pages:
    link: "/ links /"
    timeline archive: "/ timeline /"
```

The first argument is the entry name; the latter argument is a relative path to the corresponding folder in the `source` folder in the hexo directory.

### Integrated Services

#### comment

Used to set up commenting system.

Specific settings refer to [Comment system](/en/services/#Comment-system)

`Duoshuo` ` disqus` is currently available parameter.

- use:
- shortname:
- duoshuo_thread_key: Used to set the use of tread key, the default is `path`, can be set to` id`.
- duoshuo_embed_js_url: say js.

#### search

Used to set up the search system.

Specific settings refer to [Search System](/en/services/#Search-system)

Currently, you can use `google` `swiftype` `local`.

- use
- swiftype_key

#### leancloud

Specific settings [Set Leancloud](/en/services/#Leancloud)

- enable: Defaults to false.
- app_id: APP ID.
- app_key: APP Key.
- av_core_mini: Statistics js.

#### busuanzi

Specific settings refer to [Busuanzi](/en/services/#Busuanzi)

- enable: Defaults to false.
- all_site_uv: The default is false.
- post_pv: The default is false.
- busuanzi_pure_mini_js: Statistics js.
