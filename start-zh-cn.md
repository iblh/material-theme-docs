---
title: 开始使用
version:
permalink: start
id: 1
lang: zh-cn
---
在 Hexo 中，通常有两份配置文件，一个是站点根目录下的 `_config.yml`；另外一个是主题目录下的 `_config.yml`。为了描述方便，在以下说明中，将前者称为 **站点配置文件**，后者称为 **主题配置文件**。

## 安装「Material」

Hexo 安装主题的方式非常简单，只需要将主题文件放置于站点目录的 `themes` 目录下，然后修改下配置文件即可。
具体到 Material 来说，有 `Github` 和 `NPM` 两种方式。

### Github
> 可以选择 克隆 或者  下载 [稳定的发布版本](https://github.com/viosey/hexo-theme-material/releases)。

为了方便之后的更新，建议使用 **克隆** 的方式。克隆命令如下：

```shell
$ cd your-hexo-site/themes
$ git clone https://github.com/viosey/hexo-theme-material.git material
```

### NPM

```
npm install hexo-material
```

该方式会把 Material 主题下载到 `hexo` 目录下的 `node_modules` 文件夹中。
找到 `hexo-material` 文件夹，然后把文件复制到 `themes` 目录中的 `Material` 主题文件夹里。


## 启用「Material」

克隆完成后，修改主题文件夹名称，将其改为 `material` 。
然后打开 **站点配置文件**，找到 `theme` 字段，并将其值更改为 `material` 。
>文件夹名称可自由修改，并不是唯一的，只需 `theme` 字段与之对应即可。

运行 `hexo s --debug`，并访问 `http://localhost:4000`，确保站点正确运行。


## 更新「Material」

### Github

使用
```
git pull
```

即可拉取最新版本。

### NPM

NPM 更新有两种方式：

#### npm-update

```
npm update hexo-material
```

然后将文件复制到 `Material` 主题文件夹中。

#### npm-check
[npm-check](https://www.npmjs.com/package/npm-check) 是用来检查 npm 依赖包是否有更新，错误以及不在使用的，我们也可以使用 npm-check 进行包的更新。

安装 npm-check：

```
npm install -g npm-check
```

检查 npm 包的状态:

```
npm-check hexo-material
```
使用空格键可以选择需要处理的包，回车直接进行处理。


## 基本设定

### 语言

编辑 **站点配置文件**，将 `language` 设置成你所需要的语言。
可用的语言如下：

- العَرَبِيَّة (ar) 
- English (en)
- Español (es)
- Français (fr)
- Deutsche (de)
- 日本語 (ja)
- Malay (ms)
- 简体中文 (zh-CN)
- 繁體中文 (zh-TW)


>例如：选用繁體中文，则配置为：
>
```yml
language: zh-TW
```

### URL

编辑 **站点配置文件**，`url` 填写主域名，`root` 填写 子目录/根域名

>例如：站点域名为 `http://example.com/hexo`：
>
```yml
url: http://example.com
root: /hexo
```

若你的站点没有运行在子目录中，则 `root` 填写为 `/`。

### 作者名称

编辑 **站点配置文件**，设置 `author` 为你的昵称。


### 站点描述设置

编辑 **站点配置文件**，设置 `description` 字段为你的站点描述。站点描述可以是你喜欢的一句签名:)

### RSS

安装插件：[hexo-generator-feed](https://github.com/hexojs/hexo-generator-feed)，配置方式如插件 `README.md` 所示。
然后在 [url: rss](/intro/#url) 中添加生成的 feed 路径。