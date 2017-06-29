---
title: Services
version: 1.4.0
permalink: en/services
id: 5
lang: en
---

"Material" has built in lots of Integrated Services. You can easily set up it.

## RSS

First, you should install the plugin [hexo-generator-feed](https://github.com/hexojs/hexo-generator-feed). Read the plugin's `README.md` to install and configure it.

Then configure `theme config`  [url: rss](/en/intro/#url) with the URI.

## topPost

Use this to pin post at the top of the list of posts.
If you want to use this WIP feature, please install `hexo-helper-post-top` :

```bash
npm install hexo-helper-post-top --save
```

Now you can use `front-matter` `top: true` to pin your posts what you want to.

----

You can configure third-party services by navigating to `Integrated Services` in the **theme config**

## Comment system

Used to set up a comment system.

See [comment system](/en/services/#Comment-system) for more information.

- `use`: `disqus` `disqus_click` `changyan` `163gentie` or `livere`

> When Using `disqus_click`, post won't load Disqus automatically. The pages will load Disqus when the vistors click the button. This feature will help to improve some people's browse exprience from where they can't load Disqus normally, such as China.

> The livere built in the Material is `city_verison`.

- `shortname`: the shortname of duoshuo and disqus
- `changyan_appid`: the APPID of changyan
- `changyan_conf`: the CONF of changyan
- `changyan_thread_key_type`: path #identifier of posts. `path` as default.
- `gentie_productKey`: You can find the productkey in `install code` at 163gentie's console, something like `gentie_productKey: "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"`
- `gentie_thread_key_type`: Default is path. If using ID, you should add `id` front-matter for every post. Then 163gentie will use it as identifier.
- `livere_data_uid`: You can find the `datd_uid` from the provided code.

## Search system

### Google

Call the Google search engine to search your site.

```yaml
search:
    use: google
```

### Local Search

The [hexo-generator-search](https://github.com/PaicHyperionDev/hexo-generator-search) plugin needs to be installed when using local search.

```yaml
search:
    use: local
```

### Swiftype

Sign up for [Swiftype](https://swiftype.com/). In your Swiftype installation code, you'll find a line like `_st ( 'install', 'myKey', '2.0.0');`.

```yaml
search:
    use: swiftype
    swiftype_key: myKey
```

## Browse statistics

### Site Analytics

Material theme has a built in Baidu's, Google's website analytics and CNZZ's analytics service.You can easily set the ID to enable it.

- `use`: Set which analytics you want to use.  Available values are baidu | google | cnzz
- `site_id`: the site_id that analytics service provide.

> - Google will give the `site ID` with `UA-` begin; 
> - Baidu will give your a JavaScript URI like `hm.js?xxxxxxxxx` and `xxxxxxxx` is the site_id that you need.
> - in CNZZ's code, there will be `z_stat.php?id=xxxxxxxxxxxx` and `&web_id=xxxxxxxxx`. Both of these `xxxxxxxx` should be the same. And this `xxxxxxxxx` is the site_id.

### Other Analytics

You should set the `use` with nothing. Then you can add the analytics code in `head.yml`. You can read the [expert](/en/expert/) about how to use `head.yml`.

### Leancloud

Open the LeanCloud website and go to the [registration page](https://leancloud.cn/login.html#/signup) to register. After the mailbox is activated, click on the avatar to access the console page as following:

![](https://qiniu.viosey.com/img/leancloud-config-1.png)

Create a new application (the default type is JavaScript SDK), click Apply to enter;

Create a Class named `Counter`
Note: `ACL Permissions` must be `unrestricted`

![](https://qiniu.viosey.com/img/leancloud-config-2.png)
![](https://qiniu.viosey.com/img/leancloud-config-3.png)

You can find `app_id` and `app_key` in `application -> Settings -> Application Key`.

```yaml
leancloud:
    enable: true
    app_id: #app_id
    app_key: #app_key
    av_core_mini: "https://cdn1.lncld.net/static/js/av-core-mini-0.6.1.js"
```

> Add your blog domain to `application -> Settings -> Security Center` to ensure data security calls.

#### Busuanzi

To use the view statistics, simply set:

```yaml
busuanzi:
    enable: true
    all_site_uv: false
    post_pv: false
    busuanzi_pure_mini_js: "https://dn-lbstatics.qbox.me/busuanzi/2.3/busuanzi.pure.mini.js"
```

Parameters are:

- `all_site_uv`: counts the number of unique visitors to the site
- `post_pv`: the number of page views for each post
- `busuanzi_pure_mini_js`: You can save the js to your webserver or CDN, then set the URI here.
