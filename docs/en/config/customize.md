# Customize Settings

## copyright_since

Specify the date when the site was setup.

>  For example, if you set it as 2015, then footer will show '© 2015 - 2017'

When it is empty, the footer will only show the current year.

## footer_text
You can specify the text you want to show in footer, HTML tag is supported.
For example, you can setup ICP license number as:

```yml
footer_text: '<a href="http://www.miitbeian.gov.cn" rel="nofollow">某ICP备xxxxxxxx号-x</a>'
```

## qrcode

Use this to show qrcode in your article.

- enable: show qrcode button in post or not.
- use: choose which method to generate the Qrcode. Available value of "use": plugin | online

> When using `plugin`, you need to install `hexo-helper-qrcode` to support this feature. Using `npm install hexo-helper-qrcode --save` to install the plugin.
> When using `online`, the Qrcode will generate by `pan.baidu.com`. We DO NOT recommend you to use it.

## Code

Use `Google Prettify` to highlight the code
if true, check highlight option in _config.yml. Make sure that default code highlight plugin is disabled.

```yml
prettify:
    enable: false # Available value: true | false,
    theme: "vibrant-ink" # default value: "vibrant-ink"   # theme-name without '.css'
```

## Post License
You can specify the text you want to show in the end of your posts and pages, HTML tag is supported.
For example, you can setup a CC license as:

```yml
license: 'This blog is under a <a href="/creativecommons.html" target="_blank">CC BY-NC-SA 3.0 Unported License</a>'
```
> You can also use Front-Matter `license` to override this setting.
