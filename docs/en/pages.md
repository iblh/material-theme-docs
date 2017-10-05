# Pages

## Create the "Links" page

### Create the page

Create a folder named `links` within the `source` folder. Then create a file named `index.md` inside this folder:

```yaml
---
title: links
date:
layout: links
---
```

> `title` can be changed, `layout` can not be modified.

If you want to add a link to the "Link" page, please refer to the [page settings](/en/intro/#pages).

### Add data

Create a folder named `_data` (rename is forbidden) within the `source` folder. Then create a file named `links.yaml` inside this folder.

The format for a single link is:

```yaml
Name:
    link: http://example.com
    avatar: http://example.com/avatar.png
    descr: "This is a description"
```

Change `Name` to the name of the link. You can create as many links as you want.

## Create the "Gallery" page

### Create the page

Create a folder named `gallery` within the `source` folder. Then create a file named `index.md` inside this folder:

```yaml
---
title: gallery
date:
layout: gallery
---
```

> `title` can be changed, `layout` can not be modified.

If you'd like to add an entry to the "Gallery" page, please refer to the [page settings](/en/intro/#pages).

### Add data

Create a folder named `_data` (rename is forbidden) within the `source` folder. Then create a file named `gallery.yaml` inside this folder.

The format for a single image is:

```yaml
Name:
    full_link: http://example.com/full-image.png
    thumb_link: http://example.com/thumb-image.png
    descr: "This is a description"
```

Change `Name` to the image name. You can create as many images as you want.

## Create the "Tag Cloud" page

### Create the page

Create a folder named `tags` within the `source` folder. Then create a file named `index.md` inside this folder:

```yaml
---
title: tags
date:
layout: tags
---
```

> `title` can be changed, `layout` can not be modified.

If you'd like to add an entry to the Tag Cloud page, please refer to the [page settings](/en/intro/#pages).

## Create the "Timeline" page

### Create the page

Create a folder named `timeline` within the `source` folder. Then create a file named `index.md` inside this folder:

```yaml
---
title: timeline
date:
layout: timeline
---
```

> `title` can be changed, `layout` can not be modified.

If you'd like to add an entry to the Timeline page, please refer to the [page settings](/en/intro/#pages).