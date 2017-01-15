---
title: Start
version:
permalink: en/start
id: 1
lang: en
---

In Hexo, there are usually two configuration files, both called `_config.yml`. The first one is in the site root directory; the other is in the theme directory. For convenience of description, in the following description, the former is referred to as the **site config** and the latter as the **theme config**.

## Installing "Material"

Installation of an Hexo theme is quite simple. You simply need to put the theme directory inside the `themes` directory of your site and modify the theme config.

There are three ways to install the Material theme: using `Github` or `NPM`.

### Direct download

Download a [stable release](https://github.com/viosey/hexo-theme-material/releases) and extract the content inside the `themes/material` directory.

### Github (recommended)

Cloning the Github repository is more suitable to benefit from further updates. Go in the site root directory and use the following command:

```bash
git clone https://github.com/viosey/hexo-theme-material.git themes/material
```

### NPM

Go in the site root directory and use the following commands:

```bash
npm install hexo-material
cp -R node_modules/hexo-material/ themes/material
```

## Enable "Material"

Once you have the `themes/material` folder, open the **site config**, find the `theme` field, and change its value to `material`.

> The folder `themes/material` can be named differently if you wish. You simply have to adapt the `theme` field accordingly.

Run `hexo s --debug` and go to [`http://localhost:4000`](http://localhost:4000) to make sure the site is running properly.

## Update "Material"

### Direct download

Save your `_config.yml` file somewhere. Then download a new [stable release](https://github.com/viosey/hexo-theme-material/releases) and extract the content inside the `themes/material` directory. Finally reconcile the new version of the `_config.yml` with the one you saved.

### Github (recommended)

Simply use:

```bash
cd themes/material
git stash
git pull
git stash pop
```

The previous commands will put aside your custom config, pull the update reapply your modifications. Fix conflicts if needed.

### NPM

NPM updates can be done in two ways:

#### NPM update

Save your `_config.yml` file somewhere. Then use:

```bash
npm update hexo-material
rm -R themes/material
cp -R node_modules/hexo-material/ themes/material
```

Finally reconcile the new version of the `_config.yml` with the one you saved.

#### npm-check

[Npm-check](https://www.npmjs.com/package/npm-check) is used to check NPM dependency package for updates or errors.

Install npm-check:

```bash
npm install -g npm-check
```

Save your `_config.yml` file somewhere. Then use:

```bash
npm-check hexo-material
```

Use the space bar to select the package to update and press enter.

## Basic settings

### Language

Edit the **site config** and set `language` to the language you want.

Available languages ​​are:

- Deutsche: de
- English: en
- Español: es
- Français: fr
- Malay: ms
- 日本語: ja
- العَرَبِيَّة: ar
- 简体中文: zh-CN
- 繁體中文: zh-TW


> For example, to use Traditional Chinese, the configuration would be:
>
```yaml
language: zh-TW
```

### URL

Edit the **site config**, put your main domain name as the `url` parameter and put the site root directory as the `root` parameter.

> For example, for a site accessible using `http://example.com/hexo`, the configuration would be:
>
```yaml
url: http://example.com
root: /hexo
```
> For a site accessible using `http://example.com/`, the configuration would be:
>
```yaml
url: http://example.com
root: /
```

### Author name

Edit the **site config** and set the `author` parameter with whatever you want to be called.

### Site description

Edit the **site config** and set the `description` parameter with the description of your site description. The site description can be a signature you like :)

### RSS

To use an RSS system, install the following plugin: [hexo-generator-feed](https://github.com/hexojs/hexo-generator-feed).

Follow instructions from the plugin `README.md`. Then add the generated feed path as the `rss url` parameter in the **theme config**. See [here](/en/intro/#url) for more information.
