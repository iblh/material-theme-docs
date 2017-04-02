---
title: 集成服务
version: 1.3.2
permalink: services
id: 5
lang: zh-cn
---
在 **主题配置文件** 中定位到 `Integrated Services` 即可进行第三方服务的配置。

## 评论系统

Material 主题内提供了 disqus、多说和畅言的评论服务。阅读 [Intro-comment](/intro/#comment) 搜索评论配置有关介绍。

## 搜索系统

阅读 [Intro-comment](/intro/#search) 搜索系统配置介绍。

### Google

调用 Google 搜索引擎对您的站点进行搜索。

在 **主题配置文件** 中修改 `search: use` 的值为 `google` 即可。

### 本地搜索

使用本地搜索需要安装 [hexo-generator-search](https://github.com/PaicHyperionDev/hexo-generator-search) 插件。
然后在 `站点配置` 文件中添加
```yml
search:
	path: search.xml
	field: post
```

### Swiftype

注册 [Swiftype](https://swiftype.com/)，然后在 **主题配置文件** 中修改 `search: use` 的值为 `swiftype`，并填入你的 `swiftype_key`。

>在你的 Swiftype Install Code 中，有这么一行代码 `_st('install','*****','2.0.0');`

>`*****` 即为 `swiftype_key`

## 浏览统计
### Leancloud

#### 注册

打开 LeanCloud 官网，进入[注册页面](https://leancloud.cn/login.html#/signup)注册。完成邮箱激活后，点击头像，进入控制台页面，如下：

![](https://qiniu.viosey.com/img/leancloud-config-1.png)

#### 创建新应用
创建一个新应用 (默认类型为JavaScript SDK)，点击应用进入；

创建名称为 `Counter` 的 Class
注意：`ACL 权限` 必须为 `无限制` 
![](https://qiniu.viosey.com/img/leancloud-config-2.png)
![](https://qiniu.viosey.com/img/leancloud-config-3.png)

#### 修改配置文件
编辑 `主题配置文件` ，修改 `leancloud` 条目
将 `enable` 改为 `true`，再填入 `app_id` 与 `app_key`。
>在 `应用->设置->应用 Key` 可看到 `APP ID` 与 `APP Key`，

#### Web 安全性
为了保证应用的统计计数功能仅应用于自己的博客系统，你可以在 `应用->设置->安全中心` 的Web安全域名中加入自己的博客域名，以保证数据的调用安全。

### 不蒜子

使用 不蒜子 浏览次数统计，仅需在 **主题配置文件** 中将 `busuanzi: enable: ` 的值设置为 `true`。

其中：

- `all_site_uv` 可统计全站的独立访客人数，即可在 `blog_info` 模块的 `Menu` 菜单中看到。

- `post_pv` 统计每篇文章的页面浏览次数，在文章页的 `分享按钮` 菜单中可看到。

- `busuanzi_pure_mini_js` 调用不蒜子统计 js 文件，可将改文件放到自己的 CDN 然后修改值。