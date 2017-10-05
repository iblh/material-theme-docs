---
title: Start
version: 1.4.0
permalink: en/start
id: 1
lang: en
---

## Installing "Material"

Installation of an Hexo theme is quite simple. You simply need to put the theme directory inside the `themes` directory of your site and modify the theme config.
There are three ways to install the Material theme: using `Github` or `NPM`.

### Direct download

Download a [stable release](https://github.com/viosey/hexo-theme-material/releases) and extract the content inside the `themes/material` directory.

### NPM

Go in the site root directory and use the following commands:

```bash
npm install hexo-material
cp -R node_modules/hexo-material/ themes/material
```

## Enable "Material"

Once you have the `themes/material` folder, open the **site config**, find the `theme` field, and change its value to `material`.

> The folder `themes/material` can be named differently if you wish. You simply have to adapt the `theme` field accordingly.

**The `_config.yaml` file does not exist in the theme, you need to manually duplicate the `_config.template.yaml` file and rename it to `_config.yaml`**

Run `hexo s --debug` and go to [`http://localhost:4000`](http://localhost:4000) to make sure the site is running properly.

## Update "Material"

### Direct download

Save your `_config.yaml` file somewhere. Then download a new [stable release](https://github.com/viosey/hexo-theme-material/releases) and extract the content inside the `themes/material` directory. Finally reconcile the new version of the `_config.yaml` with the one you saved.

The previous commands will put aside your custom config, pull the update reapply your modifications. Fix conflicts if needed.

### NPM

NPM updates can be done in two ways:

#### NPM update

Save your `_config.yaml` file somewhere. Then use:

```bash
npm update hexo-material
rm -R themes/material
cp -R node_modules/hexo-material/ themes/material
```

Finally reconcile the new version of the `_config.yaml` with the one you saved.

#### npm-check

[Npm-check](https://www.npmjs.com/package/npm-check) is used to check NPM dependency package for updates or errors.

Install npm-check:

```bash
npm install -g npm-check
```

Save your `_config.yaml` file somewhere. Then use:

```bash
npm-check hexo-material
```

Use the space bar to select the package to update and press enter.

## Basic settings

### Language

Edit the **site config** and set `language` to the language you want.

Available languages ​​are:

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


> For example, to use Traditional Chinese, the configuration would be:
>
```yaml
language: zh-TW
```
