---
title: Expert
version:
permalink: en/expert
id: 4
lang: en
---
## Add custom code

If you want to add custom `font-face` or statistical code (such as `Google Analytics`) to your site.

You need to create a folder named `_data` (no rename) in the` source` folder in the hexo directory.

And then create a file called head.yml in the file.

The single code format is:

```yaml
Name:
     "Put your code here"
```

The code will be displayed before `</head>`,
`Name` will appear as a comment above the code.

## Palette