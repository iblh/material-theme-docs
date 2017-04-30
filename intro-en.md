---
title: Intro
version: 1.4.0
permalink: en/intro
id: 2
lang: en
---

Now we will introduce you about how to configure the theme, include `Site Information` `Style Settings` `Menu Settings`.

## Site information

### head

Used to configure the generated HTML file header information.

- `favicon`: the favicon
- `high_res_favicon`: the favicon using high quality format
- `apple_touch_icon`: the iOS Home button icon
- `keywords`: the site keywords
- `google_site_verification`: Google Search Console Verification.

> 1. After logged in [Google Search Console](https://www.google.com/webmasters/tools/), when to the `Site Verification`, and use `<meta>` tag to finish the verification. Then Google will give you something like:
```html
<meta name="google-site-verification" content="xxxxxxxxxxxxxxxxxxxxxxxxxxxx" />
```
> 2. Simply set the `google_site_verification` with the things like `xxxxxxxxxxxxxxxxxxxxxxxxxxxx`.

### url

Used to set jump links.

- `rss`: the rss or atom url.
- `daily_pic`: the redirect url from click on the daily picture
- `logo`: the redirect url from click on the logo

> You can read the [Service](/service/) about how to set up the RSS.

## Style Settings

### scheme

Material theme provides a variety of theme designs, also known as "Scheme". Material currently supports three schemes.

#### Nexus (under development)

This is the most standard Material Design style.

#### Paradox (default)

This is the original style of Material. The layout is centered and illustrated.

#### Isolation

This is a variant of Paradox using Jane style. It is concise and clear.

----

If you want to use one of the themes, delete the '#' before the scheme name.
For example, to select the Paradox scheme, simply use:

```yaml
#scheme: Nexus
scheme: Paradox
#scheme: Isolation
```

### uiux

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

> [color palette](https://material.google.com/style/color.html#color-color-palette).

### js_effect

Used to control the JavaScript features.

- `fade`: part of the module to load the page fade effect (default: true)
- `smoothscroll`: page smooth scrolling effects (default: false)

### reading

Used to set the reading experience.

- `entry_excerpt`: the home page outputs the character length of the digest (default: 80)

### thumbnail

Used to set up article thumbnail correlation.

- `purecolor`: the color to fill (solid thumbnail used if no one is set)
- `random_amount`: the number of random pictures taken from the `themes/material/source/img/random` folder

### background

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

### fonts

- `fonts`: Used to set the site fonts.

> The default values are `Roboto, Helvetica Neue, Helvetica, PingFang SC, Hiragino Sans GB, Microsoft YaHei, Microsoft Yahe, Arial`
> The font settings are more standardized for Material Design, no special requirements without additional changes.
> When update the fonts, you should add fonts embed in `head.yml`. You can read [expert](/en/expert/) about how to use `head.yml`

- `host`: Used to set which fonts lib will be uesd in the theme.

> We have two available value of "host": `google` and `baomitu`.
> - `google`: use `fonts.googleapi.com` to load `Roboto` and `Material Icon`.
> When using `Isolation UX`, the theme will load `Font-Awesome` locally.
> - `baomitu` use `lib.baomitu.com`(a public cdn which maintained by Qihoo 360 75Team) to load `Roboto` and `Material Icon`
> When using `Isolation UX`, the theme will load `Font-Awesome` from `lib.baomitu.com` as well.

If you want to use one of the font host, just delete the '#' before the hostname your want, and add '#' to another.

Both of the `fonts.googleapi.com` and `lib.baomitu.com` are HTTPS supported. Otherwise, `lib.baomitu.com` support HTTP/2 while `fonts.googleapi.com` support HTTP/2+QUIC/37.

### card_elevation

Used to set elevation of the card on the list of the posts.  

### copyright_since

Specify the date when the site was setup.

>  For example, if you set it as 2015, then footer will show '© 2015 - 2017'

When it is empty, the footer will only show the current year.

### qrcode

Use this to show qrcode in your article.  
Need `hexo-helper-qrcode` to support this feature:

## Menu Settings

### sns

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

### sns_share

Used to choose which items will be displayed in share menu.

- `twitter`
- `facebook`
- `googleplus`
- `weibo`
- `linkedin`
- `qq`
- `telegram`

### sidebar

#### dropdown

Used to set the Paradox sidebar drop-down menu (empty by default).

Refer to the configuration style

```yaml
dropdown:
    Email Me:
    link: "#"
    icon: email
```

#### homepage

Used to set the home page button.

- `use`: set `true` to display this button is the sidebar
- `icon`: add an Material Design icon before the name of the button. Let it empty for no icon.
- `divider`: set `true` to add a divider after the button

#### archives

Used to set the archives button.

- `use`: set `true` to display this button is the sidebar
- `icon`: add an Material Design icon before the name of the button. Let it empty for no icon.
- `divider`: set `true` to add a divider after the button

#### categories

Used to set the categories button.

- `use`: set `true` to display this button is the sidebar
- `icon`: add an Material Design icon before the name of the button. Let it empty for no icon.
- `divider`: set `true` to add a divider after the button

#### pages

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

#### article_num

Used to display the number of articles.

- `use`: set `true` to display this button is the sidebar
- `divider`: set `true` to add a divider after the button

#### footer

Used to customize the sidebar footer.

- `divider`: set `true` to add a divider before the footer
- `theme`: set `true` to display a link to the theme site
- 

## Integrated Services
Read the [Service](/services/)
