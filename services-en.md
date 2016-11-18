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

Material theme has a built-in `Duoshuo` Material Design appearance .

To use [Duoshuo](https://duoshuo.com/), simply set the `comment: use:` value to`"duoshuo"`.

Then fill in your shortname with `comment: shortname:`

> Material theme has two kind of `tread key`, the default is the article relative path.
The other is id, which needs to be added in `front-matter`
>
```yaml
id: id_number
```
>If it is migrated from other blog systems, the thread_Key has to keep the same.

### Disqus

To use [Disqus](https://disqus.com/), simply set the `comment: use:` value to`"disqus"`.

Then fill in your Disqus shortname in `comment: shortname:`

------

Note: the `shortname` here is not your login id, is your comment services field which removed the secondary domain name `.duoshuo.com` or`.disqus.com` part

> For example: Duoshuo domain name `example.duoshuo.com` / Disqus domain name` example.disqus.com`

> ```yaml
shortname: example
```

## Search system

Read [Intro-comment](/en/intro/#comment) to search for system configuration descriptions.

### Google

Call the Google search engine to search your site.

Change the value of `search: use` to `google`  in the **theme config**.

### Local Search

The [hexo-generator-search](https://github.com/PaicHyperionDev/hexo-generator-search) plugin needs to be installed when using local search.
Then add below code to the `site config` file

```yaml 
search:
  path: search.xml
  field: post
```



### Swiftype

Sign up for [Swiftype](https://swiftype.com/) and change the value of `search: use` to` swiftype` in your **theme config** and fill in your `swiftype_key`.

> In your Swiftype Install Code, there is a line of code `_st ( 'install', '*****', '2.0.0');`

> `*****` is called `swiftype_key`



## Browse statistics

### Leancloud

#### Register

Open the LeanCloud website and go to the [Registration page](https://leancloud.cn/login.html#/signup) to register. After the mailbox is activated, click on the avatar to access the console page as follows:

![](Https://qiniu.viosey.com/img/leancloud-config-1.png)

#### Create a new app

Create a new application (the default type is JavaScript SDK), click Apply to enter;

Create a Class named `Counter`
Note: `ACL Permissions` must be` unrestricted `
![](Https://qiniu.viosey.com/img/leancloud-config-2.png)
![](Https://qiniu.viosey.com/img/leancloud-config-3.png)

#### Modify the theme configuration file

Edit the `theme config` and change the `leancloud` field,
Change `enable` to` true` and fill in `app_id`  and ` app_key`.

> In the `application -> Settings -> Application Key` can see the `APP ID` and  `APP Key`,

#### Web Security

In order to ensure that the application of statistical counting function applies only to their own blog system, you can in the `application -> Settings -> Security Center` of the Web security domain name to add your blog domain to ensure data security calls.

### Busuanzi

To use the View statistics, simply set the value of `busuanzi: enable:` to `true` in the **theme config**.

among them:

- `all_site_uv` counts the number of unique visitors to the site, which can be found in the menu of the` blog_info` module.
- `post_pv` Statistics the number of page views for each post, as seen in the article `Share button` menu.
- `busuanzi_pure_mini_js` Call not garlic statistics js file, you can change the file into your CDN and then modify the value.