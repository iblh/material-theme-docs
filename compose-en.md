---
title: Compose
version: 1.4.0
permalink: en/compose
id: 3
lang: en
---

## Create an article

### Use the command line

```bash
hexo new <title>
```

### Create it manually

Create a file with the extension `.md` inside the `source/_posts` folder.

### Front-matter

See [front-matter](https://hexo.io/en/docs/front-matter.html) for more information.

| Setting    | Description                                | Default           |
| ---------- | ------------------------------------------ | ----------------- |
| layout     | Layout                                     |                   |
| title      | Title                                      |                   |
| date       | Published date                             | File created date |
| update     | Updated date                               | File updated date |
| comments   | Enables comment feature for the post       | true              |
| tags       | Tags (Not available for pages)             |                   |
| categories | Categories (Not available for pages)       |                   |
| permalink  | Override the default permalink of the post |                   |
| toc        | Display TOC button		                  | true   		      |
| comment    | Display comment	                          | true              |
| notag      | Do not generate Tags menu                  | false             |
| top        | Pin post on the top of the list            | false             |

P.S. To use `Pin on top` feature please visit [topPost](/intro/#topPost)

### Thumbnail function

In the Material theme, each Scheme has a thumbnail function. Simply add the `thumbnail:` parameter to the `front-matter` and fill in the thumbnail address.

#### Paradox

This scheme uses the default random thumbnails if there is no custom thumbnail. The random thumbnail directory is located under the `source/img/random` folder. You can add your favorite images in the format `material-<num>.png`. Then modify the `random_amount` parameter in the **theme config**.

#### Isolation

This Scheme will only show thumbnails that have been customized.

## Create the "About" page

Create a new `about` page:

```shell
hexo new page "About"
```

If you want to add a link to the "Link" page, please refer to the [page settings](/en/intro/#pages).

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

Create a folder named `_data` (rename is forbidden) within the `source` folder. Then create a file named `links.yml` inside this folder.

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

Create a folder named `_data` (rename is forbidden) within the `source` folder. Then create a file named `gallery.yml` inside this folder.

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
