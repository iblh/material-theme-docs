---
title: 集成服务
version: 1.3.3
permalink: services
id: 5
lang: zh-cn
---

「Material」主题内置了多种第三方服务，并且可以轻松的启用。

## RSS

安装插件：[hexo-generator-feed](https://github.com/hexojs/hexo-generator-feed)，配置方式如插件 `README.md` 所示。
然后在 [url: rss](/intro/#url) 中添加生成的 feed 路径。

----

在 **主题配置文件** 中定位到 `Integrated Services` 即可进行第三方服务的配置。

## MaterialCDN

为了加速您的博客，现在您可以使用 CDN 来加速 Material 主题引用的静态文件。
只需要将 `use` 设置为 `true`，并在 `base` 中填入你的 CDN 的 URL 路径即可。

> **注意！`base` 中填入的 URL 末尾不需要带 `/` ！**

例如，您可以这么配置：

```yaml
materialcdn: 
    use: true # 默认为 false
    base: https://materialcdn.nfz.moe/hexo/1.3.2
```

## 评论系统

定位到 **`主题配置文件`** 中 `Integrated Services` 的 `comment`，即可以设置评论。

### 多说

Material 内置了一套 多说 的 Material Design 样式。

> 请注意！多说将于 2017 年 6 月 1 日启停止服务。届时 Material 主题将移除对多说的支持！

使用 [多说](https://duoshuo.com/)，需在 **主题配置文件** 中填写 `comment: use: ` 字段，值设置为 `duoshuo`。

然后在 `comment: shortname: ` 填入你的多说 shortname

> 主题的多说评论使用两种 `tread key`。默认为文章的相对路径 path。另一种为 id，需要在文章中的 `front-matter` 中添加 

```yml
id: id_number
```

> 如果是从其他博客系统迁移过来，文章的需要和多说后台的 Thread_Key 保持一致。

`duoshuo_embed_js_url` 用于设置调用的多说 JS 的地址。如果没有特殊需求，可以使用默认。 

### Disqus

Material 主题提供了两种使用 [Disqus](https://disqus.com/) 主题的方式，在 **主题配置文件** 中填写 `comment: use: ` 字段，值设置为 `disqus` 或 `disqus_click`。

> 使用 Disqus_Click 时，文章页面不会主动加载 Disqus 评论，直到按下按钮。这项设置有助于改善处在 **`公开、平等、有序 的 网络审查 地区`** 下的浏览者的体验。

在 `comment: shortname: ` 填入你的 Disqus shortname

----

需要注意的是此处的 `shortname` 不是你的登录的 id，是你的评论二级域名去掉 `.duoshuo.com` 或 `.disqus.com` 部分

>例如：多说域名 `example.duoshuo.com` / Disqus 域名 `example.disqus.com`

> ```yml
shortname: example
```

### 畅言 

使用 [畅言](http://changyan.kuaizhan.com)，需在 **主题配置文件** 中填写 `comment: use: ` 字段，值设置为 `changyan`。

- changyan_appid: 畅言的 APPID
- changyan_conf: 畅言的 CONF
- changyan_thread_key_type: path #用于设置畅言的 tread key，默认为 path。

## 搜索系统

Material 主题内置了 `google ` `swiftype` `local` 三种搜索系统。

```yaml
- use
- swiftype_key
```

### Google

调用 Google 搜索引擎对您的站点进行搜索。

在 **主题配置文件** 中修改 `search: use` 的值为 `google` 即可。

### 本地搜索

使用本地搜索需要安装 [hexo-generator-search](https://github.com/PaicHyperionDev/hexo-generator-search) 插件。

然后在 `站点配置` 文件中添加
```yml
search:
	path: search.xml
	field: all
```

### Swiftype

注册 [Swiftype](https://swiftype.com/)，然后在 **主题配置文件** 中修改 `search: use` 的值为 `swiftype`，并填入你的 `swiftype_key`。

> 在你的 `Swiftype Install Code` 中，有这么一行代码 `_st('install','*****','2.0.0');` 。其中 `*****` 即为 `swiftype_key`

## 数据统计与分析

用于设置访客分析服务，支持 Google Analysis 和 百度站长工具。

```yaml
baidu_id: 百度 ID
google_id: Google Analysis 密钥
```

### 百度统计

登录 [百度统计](http://tongji.baidu.com/)，在站点的代码获取页面复制 `hm.js?` 后面那串统计脚本 id，填入 `baidu_id`。

### Google 分析

在 `google_id` 字段填入你的 Google 跟踪 ID。跟踪 ID 通常是以 UA- 开头。

### 其它统计服务

确保 `baidu_id` `google_id` 两个字段为空，然后在在 `head.yml` 中填入你的统计服务代码。如何使用 `head.yml`，请访问[进阶设定](/expert/)中关于 自定义代码 的部分。

### PV&UV 统计

在 Material 主题中提供 PV&UV 显示。

#### Leancloud

```yaml
- enable: 默认为 false。
- app_id: APP ID。
- app_key: APP Key。
- av_core_mini: 统计 js。
```

打开 LeanCloud 官网，进入[注册页面](https://leancloud.cn/login.html#/signup)注册。完成邮箱激活后，点击头像，进入控制台页面，如下：

![](https://qiniu.viosey.com/img/leancloud-config-1.png)

创建一个新应用 (默认类型为JavaScript SDK)，点击应用进入；

创建名称为 `Counter` 的 Class
注意：`ACL 权限` 必须为 `无限制` 

![](https://qiniu.viosey.com/img/leancloud-config-2.png)
![](https://qiniu.viosey.com/img/leancloud-config-3.png)

编辑 `主题配置文件` ，修改 `leancloud` 条目，将 `enable` 改为 `true`，再填入 `app_id` 与 `app_key`。在 `应用->设置->应用 Key` 可看到 `APP ID` 与 `APP Key`

> 为了保证应用的统计计数功能仅应用于自己的博客系统，你可以在 `应用->设置->安全中心` 的Web安全域名中加入自己的博客域名，以保证数据的调用安全。

#### 不蒜子

```yaml
- enable: 默认为 false。
- all_site_uv: 默认为 false。
- post_pv: 默认为 false。
- busuanzi_pure_mini_js: 统计 js。
```

使用 不蒜子 浏览次数统计，仅需在 **主题配置文件** 中将 `busuanzi: enable: ` 的值设置为 `true`。

其中：

- `all_site_uv` 可统计全站的独立访客人数，即可在 `blog_info` 模块的 `Menu` 菜单中看到。
- `post_pv` 统计每篇文章的页面浏览次数，在文章页的 `分享按钮` 菜单中可看到。
- `busuanzi_pure_mini_js` 调用不蒜子统计 js 文件，可将该文件保存至你的 WebServer 或 CDN 中，然后在这里填入 URL。
