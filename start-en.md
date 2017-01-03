---
title: Start
version:
permalink: en/start
id: 1
lang: en
---
In Hexo, there are usually two configuration files, one is the site root directory `_config.yml`; the other is the theme directory` _config.yml`. For convenience of description, in the following description, the former is referred to as a **site config**, which is called a **theme config**.

## Installing "Material"

Hexo installation of the theme is very simple, just put the theme file in the site directory `themes` directory, and then modify the configuration file can be.
Specific to the Material, there are `Github` and `NPM` two ways.

### Github
> You can choose to clone or download a [stable release](https://github.com/viosey/hexo-theme-material/releases).

In order to facilitate the subsequent update, the proposed ** clone ** approach. The cloning command is as follows:

```Shell
$ cd your-hexo-site/themes
$ git clone https://github.com/viosey/hexo-theme-material.git material
```

### NPM

```
npm install hexo-material
```

This will download the Material theme to the `` node_modules`` folder in the `hexo` directory.
Locate the `hexo-material` folder, and copy the file to the `Material` theme folder under the `theme` directory.


##Enable "Material"

When the clone is complete, change the theme folder name to `material`.
Then open **site config**, find the `theme` field, and change its value to` material`.
> Folder name can be freely modified, not the only, just `theme` field corresponding to it.

Run `hexo s --debug` and go to` http://localhost: 4000` to make sure the site is running properly.


##Update "Material"

### Github

use
```
git pull
```

You can pull the latest version.

### NPM

NPM updates are available in two ways:

#### npm-update

```
npm update hexo-material
```

Then copy the file to the `Material` theme folder.

#### npm-check
[Npm-check](https://www.npmjs.com/package/npm-check) is used to check npm dependency package for updates, errors, and non-use, we can also use npm-check package updates .

Install npm-check:

```
npm install -g npm-check
```

Check the status of the npm package:

```
npm-check hexo-material
```
Use the space bar to select the package to be processed, carriage return directly for processing.


## Basic settings

### Language

Edit the **site config** and set `language` to the language you want.
Available languages ​​are:

- English (en)
- Simplified Chinese (en-US)
- Traditional Chinese (zh-TW)
- Spanish (es)
- 日本語 (ja)


> For example: Select Traditional Chinese, the configuration is:
>
```yml
language: en-TW
```

### URL

Edit **site config**, `url` fill in the main domain name,` root` fill in the subdirectory / root domain name

> For example: The domain name of the site is `http: // example.com / hexo`:
>
```Yml
url: http://example.com
root: /hexo
```

If your site is not running in a subdirectory, `root` is filled in as` / `.

### Author name

Edit **site config**, set `author` to your nickname.


### Site Description Settings

Edit the **site config** and set the 'description` field to your site description. The site description can be a signature you like :)

### RSS

Install the plugin: [hexo-generator-feed](https://github.com/hexojs/hexo-generator-feed), Configuration as shown in the plugin `README.md`.
Then add the generated feed path in [url: rss](/en/intro/#url).