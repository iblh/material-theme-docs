---
title: 开始使用
version: 1.3.3
permalink: start
id: 1
lang: zh-cn
---

在使用 「Material」主题之前，请仔细阅读 Hexo 的[官方文档](https://hexo.io/zh-cn/docs/index.html)，完成对 Hexo 的安装和基本的配置。

> 在本文档中，我们假定你已经成功安装了 Hexo，并根据 Hexo 的文档创建了一个站点，并**完成了基本的设置**。

在 Hexo 中，通常有两份配置文件，一个是站点根目录下的 `_config.yml`；另外一个是主题目录下的 `_config.yml`。为了描述方便，在以下说明中，将前者称为 **站点配置文件**，后者称为 **主题配置文件**。

## 安装「Material」

Hexo 安装主题的方式非常简单，只需要将主题文件放置于站点目录的 `themes` 目录下，然后修改下配置文件即可。
Material 主题提供有 `Github` 和 `NPM` 两种下载方式。

### Github

> 你可以在 Github 下载 [稳定的发布版本](https://github.com/viosey/hexo-theme-material/releases)。

### NPM

```bash
npm install hexo-material
```

该方式会把 Material 主题下载到 `hexo` 目录下的 `node_modules` 文件夹中。
找到 `hexo-material` 文件夹，然后把里面的全部文件复制到 `themes` 目录中的 `Material` 主题文件夹里。

## 启用「Material」

克隆完成后，修改主题文件夹名称，将其改为 `material` 。
然后打开 **站点配置文件**，找到 `theme` 字段，并将其值更改为 `material` 。

> 文件夹名称可自由修改，并不是唯一的，只需 `theme` 字段与之对应即可。

**将 `material` 文件夹中的 `_config.template.yml` 重命名名为 `_config.yml`**。

现在，运行 `hexo s --debug` 并访问 `http://localhost:4000`，确保站点正确运行。

## 更新「Material」

### NPM

NPM 更新有两种方式：

#### npm-update

```bash
npm update hexo-material
```

然后将文件复制到 `Material` 主题文件夹中。

#### npm-check
[npm-check](https://www.npmjs.com/package/npm-check) 是用来检查 npm 依赖包是否有更新，错误以及不在使用的，我们也可以使用 npm-check 进行包的更新。

安装 npm-check：

```bash
npm install -g npm-check
```

检查 npm 包的状态:

```bash
npm-check hexo-material
```
使用空格键可以选择需要处理的包，回车直接进行处理。

### Github

你可以在[版本发布页](https://github.com/viosey/hexo-theme-material/releases)下载最新的主题。


## 基本设定

### 语言

编辑 **站点配置文件**，将 `language` 设置成你所需要的语言。
可用的语言如下：

- العَرَبِيَّة (ar)
- Deutsch (de)
- English (en)
- Español (es)
- Français (fr)
- 日本語 (ja)
- Malay (ms)
- Portuguese (Brazil) (pt-BR)
- 简体中文 (zh-CN)
- 繁體中文 (zh-TW)


>例如：选用繁體中文，则配置为：
>
```yml
language: zh-TW
```
