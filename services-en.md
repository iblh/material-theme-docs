---
title: Services
version:
permalink: en/services
id: 5
lang: en
---

You can configure third-party services by navigating to `Integrated Services` in the **theme config**.

## Comment system

### Duoshuo

Material theme has a built-in [Duoshuo](https://duoshuo.com/) system.

> Material theme has two kind of `duoshuo_thread_key_type`: path or id
> For example.duoshuo.com:
>
```yaml
comment:
    use: duoshuo
    shortname: example
    duoshuo_thread_key_type: path
    duoshuo_embed_js_url: "https://static.duoshuo.com/embed.js"
```
> If it is migrated from other blog systems, the thread_Key has to keep the same.

### Disqus

To use [Disqus](https://disqus.com/):

> For example.disqus.com:
>
```yaml
comment:
    use: disqus
    shortname: example
```

## Search system

See [comment](/en/intro/#comment) for more information.

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

### Leancloud

#### Register

Open the LeanCloud website and go to the [registration page](https://leancloud.cn/login.html#/signup) to register. After the mailbox is activated, click on the avatar to access the console page as following:

![](https://qiniu.viosey.com/img/leancloud-config-1.png)

#### Create a new app

Create a new application (the default type is JavaScript SDK), click Apply to enter;

Create a Class named `Counter`
Note: `ACL Permissions` must be `unrestricted`

![](https://qiniu.viosey.com/img/leancloud-config-2.png)
![](https://qiniu.viosey.com/img/leancloud-config-3.png)

#### Modify the theme configuration file

You can find `app_id` and `app_key` in `application -> Settings -> Application Key`.

```yaml
leancloud:
    enable: true
    app_id: #app_id
    app_key: #app_key
    av_core_mini: "https://cdn1.lncld.net/static/js/av-core-mini-0.6.1.js"
```

#### Web security

Add your blog domain to `application -> Settings -> Security Center` to ensure data security calls.

### Busuanzi

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
- `busuanzi_pure_mini_js`:
