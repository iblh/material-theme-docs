# Expert Settings

## Add custom code

If you want to add custom code, like `font-face` or statistical code (such as `Piwik Analytics`) to your site, you need to create a folder named `_data` (no rename) in the `source` folder in your site directory.

Then create a file called `head.yml` in the file:

```yaml
Name:
    "Put your code here"
```

The code will be displayed before `</head>` tag. `Name` will appear as a comment above the code.

Also, if you want to add custom code before `</html>` , simply create a file called `footer.yml` in `_data`. Same usage as `head.yml`

## Material icons

The list of icon used to customized the dropdown or page buttons is available [here](https://material.io/icons/).

## Code highlight

From `Version 1.3.0`, you can use `hexo-prism-plugin` to highlight your codes, visit [Hexo-Prism-Plugin Github](https://github.com/ele828/hexo-prism-plugin) to learn more.
From `Version 1.4.5`, Material built in the `Google Prettify` for code_highlight.
From `Version 1.5.0`, Material built in the `Hanibi` for code_highlight.

## Files Vendors

This is about how to use CDN to load files.

### MaterialCDN

Material Theme can using private CDN to load of static files.
Default(empty) will load the files from the origin server.

> **ATTENTION! the url you fill in should with protocol and without `/` !**

Here is an example of configuration.

```yaml
vendors:
    materialcdn: https://cdn.jsdelivr.net/gh/viosey/hexo-theme-material@latest/source
```
-----

Material Theme has used third party library below. You can fill in the with the uri of the files, then you can use public cdn to load them.

### jQuery 2.2.0
### Fontawesome 4.5.0

> you should filled in with a uri of css, such as: `https://cdn.bootcss.com/font-awesome/4.5.0/css/font-awesome.min.css`

### MathJax 2.7.0-2.7.1

> you needn't add query configuration in your uri. We have already done it for you.

### nprogress 0.2.0
### Prettify r298

> only for the `prettify.js`. theme css files will load from your origin server or MaterialCDN

### Material Icons 3.0.1

> you should filled in with a uri of css, such as: `https://cdn.bootcss.com/material-design-icons/3.0.1/iconfont/material-icons.min.css`
