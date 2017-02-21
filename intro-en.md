---
title: Intro
version: 1.3.0
permalink: en/intro
id: 2
lang: en
---

## Introduction to "Scheme"

Material theme provides a variety of theme designs, also known as "Scheme". Material currently supports three schemes.

### Nexus (under development)

This is the most standard Material Design style.

### Paradox (default)

This is the original style of Material. The layout is centered and illustrated.

### Isolation

This is a variant of Paradox using Jane style. It is concise and clear.

## Theme configuration

### Site information

#### head

Used to configure the generated HTML file header information.

- `favicon`: the favicon
- `high_res_favicon`: the favicon using high quality format
- `apple_touch_icon`: the iOS Home button icon
- `keywords`: the site keywords

#### url

Used to set jump links.

- `rss`: the rss or atom url.
- `daily_pic`: the redirect url from click on the daily picture
- `logo`: the redirect url from click on the logo

### Style

#### Scheme

If you want to use one of the themes, delete the '#' before the scheme name.

For example, to select the Paradox scheme, simply use:

```yaml
#scheme: Nexus
scheme: Paradox
#scheme: Isolation
```

#### uiux

Used to set the user interface and user experience.

- `slogan`: the slogan displayed in the `blog_info` module, now we support multi line slogan (see below).

Single line slogan:

```yaml
slogan: Slogan
```

Multi line slogan:

```yaml
slogan:
    - "First Line"
    - "Second Line"
    - "Third Line"
```

- `theme_color`: the main color
- `theme_sub_color`: the secondary color
- `hyperlink_color`: the color used for hyperlinks
- `button_color`: the color used for buttons
- `android_chrome_color`: the color of the Chrome address bar
- `buffer`: the top loading progress bar buffers
- `nprogress_color`: the color of the top loading progress bar
- `nprogress_buffer`: the top loading progress bar buffers

#### js_effect

Used to control the JavaScript features.

- `fade`: part of the module to load the page fade effect (default: true)
- `smoothscroll`: page smooth scrolling effects (default: false)

#### reading

Used to set the reading experience.

- `entry_excerpt`: the home page outputs the character length of the digest (default: 80)

#### thumbnail

Used to set up article thumbnail correlation.

- `purecolor`: the color to fill (solid thumbnail used if no one is set)
- `random_amount`: the number of random pictures taken from the `themes/material/source/img/random` folder

#### background

Used to set the site background.

- `purecolor`: the background color
- `bgimg`: the background image path (default: `themes/material/source/img/bg.png`)
- `bing`: used to enable bing pictures
    - `parameter`:
        - `color=`: black, blue, brown, green, multi, orange, pink, purple, red, white, yellow.
        - `type=`: A (animal), C (culture), N (nature), S (space), T (travel).

#### img

Used to set the site image.

- `logo`: the logo
- `avatar`: your avatar
- `daily_pic`: the daily picture
- `sidebar_header`: the header picture
- `footerico`: the prefix of the SNS icons from the `themes/material/source/img/footer` folder
- `random_thumbnail`: the path of the random thumbnail
- `footer_image`: you can put as any images as you want at the bottom of `sidebar`.

For instance, you can display the `upyun` logo as following:

```yaml
footer_image:
    upyun_logo:
        link: "https://www.upyun.com/"
        src: "/img/upyun_logo.png"
```

#### fonts

Used to set the site fonts.

The default values are `Roboto, Helvetica Neue, Helvetica, PingFang SC, Hiragino Sans GB, Microsoft YaHei, Microsoft Yahe, Arial`

The font settings are more standardized, no special requirements without additional changes.

#### card_elevation

Used to set elevation of the card on the list of the posts.  

### Menu

#### sns

Used to fill in your SNS information. Except for `email` (which is displayed in the sidebar), a specific icon will be put inside the footer for each url you put.

- `email`
- `facebook`
- `twitter`
- `googleplus`
- `weibo`
- `instagram`
- `tumblr`
- `github`
- `linkedin`
- `zhihu`
- `bilibili`
- `telegram`

#### sns_share

Used to choose which items will be displayed in share menu.

- `twitter`
- `facebook`
- `googleplus`
- `weibo`
- `linkedin`
- `qq`
- `telegram`

#### sidebar

##### dropdown

Used to set the Paradox sidebar drop-down menu (empty by default).

Refer to the configuration style

```yaml
dropdown:
    Email Me:
    link: "#"
    icon: email
```

##### homepage

Used to set the home page button.

- `use`: set `true` to display this button is the sidebar
- `icon`: add an Material Design icon before the name of the button. Let it empty for no icon.
- `divider`: set `true` to add a divider after the button

##### archives

Used to set the archives button.

- `use`: set `true` to display this button is the sidebar
- `icon`: add an Material Design icon before the name of the button. Let it empty for no icon.
- `divider`: set `true` to add a divider after the button

##### categories

Used to set the categories button.

- `use`: set `true` to display this button is the sidebar
- `icon`: add an Material Design icon before the name of the button. Let it empty for no icon.
- `divider`: set `true` to add a divider after the button

##### pages

Used to set up custom pages (empty by default). The pages will appear in the sidebar.

Refer to the configuration style. Let the icon empty if you don't need one. Set `true` to divider if you want a divider after the page button.

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

- `use`: set `true` to display this button is the sidebar
- `divider`: set `true` to add a divider after the button

##### footer

Used to customize the sidebar footer.

- `divider`: set `true` to add a divider before the footer
- `theme`: set `true` to display a link to the theme site

#### card_elevation

Use this to customize the shadow level of the parts of your page.

#### qrcode

Use this to show qrcode in your article.  
Need `hexo-helper-qrcode` to support this feature:

```bash
npm install hexo-helper-qrcode --save
```

#### topPost (Being Development)

Use this to pin post at the top of the list of posts.
If you want to use this WIP feature, please install `hexo-helper-post-top` :
```bash
npm install hexo-helper-post-top --save
```
And then change this method to `true`.
Now you can use `front-matter` `top: true` to pin your posts what you want to.

### Integrated services

#### comment

Used to set up a comment system.

See [comment system](/en/services/#Comment-system) for more information.

- `use`: `Duoshuo` `disqus` or `disqus_click`

> When Using `disqus_click`, post won't load Disqus automatically. The pages will load Disqus when the vistors click the button. This feature will help to improve some people's browse exprience from where they can't load Disqus normally, such as China.

- `shortname`: the shortname
- `duoshuo_thread_key_type`: used to set the use of tread key (`path` or `id`)
- `duoshuo_embed_js_url`: the JavaScript url

#### search

Used to set up the search system.

See [search system](/en/services/#Search-system) for more information.

Currently, you can use `google` `swiftype` `local`.

- `use`
- `swiftype_key`

#### analytics

Material theme has a built in Baidu's and Google's website analytics service.You can easily set the ID to enable it.

- `baidu_id`: the Baidu ID
- `google_id`: the Google key

#### leancloud

See [Leancloud](/en/services/#Leancloud) for more information.

- `enable`: (default: false)
- `app_id`: the app ID
- `app_key`: the app key
- `av_core_mini`: the JavaScript statistics

#### busuanzi

See [Busuanzi](/en/services/#Busuanzi) for more information.

- `enable`: (default: false)
- `all_site_uv`: (default: false)
- `post_pv`: (default: false)
- `busuanzi_pure_mini_js`: the JavaScript statistics


## Main Contributors

[Github - Contributors](https://github.com/viosey/hexo-theme-material/graphs/contributors)

- [pidupuis](https://github.com/pidupuis)
- [neoFelhz](https://github.com/neoFelhz)
- [AkarinServer](https://github.com/AkarinServer)
- [cubesky](https://github.com/cubesky)
- [Halyul](https://github.com/Halyul)
