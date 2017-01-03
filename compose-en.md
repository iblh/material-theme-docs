---
title: Compose
version:
permalink: en/compose
id: 3
lang: en
---
## Create an article

### Use the command line

```shell
Hexo new <title>
```

### Create it manually

In the hexo main directory `source -> _posts` create a file which suffix is ` .md`.

### Front-matter

[Front-matter - Official Introduction](https://hexo.io/en/docs/front-matter.html)

| Setting    | Description                              | Default           |
| ---------- | ---------------------------------------- | ----------------- |
| layout     | Layout                                   |                   |
| title      | Title                                    |                   |
| date       | Published date                           | File created date |
| update     | Updated date                             | File updated data |
| comments   | Enables comment feature for the post     | true              |
| tags       | Tags (Not available for pages)           |                   |
| categories | Categories (Not available for pages)     |                   |
| permalink  | Override the default permalink of the post |                   |
| toc        | Display TOC button		                 | true   		     |
| comment    | Display comment	                         | true             |
| notag      | Do not generate Tags menu                | false             |

 

### Thumbnail function

In the Material theme, each Scheme has a thumbnail function.
Simply add the `thumbnail:` parameter to the `front-matter` and fill in the thumbnail address.

#### Paradox

This scheme uses the default random thumbnails if there is no custom thumbnail. The random thumbnail directory is located under the theme folder `source -> img -> random`.
Random thumbnails can add your favorite images in the format `<num> .png`. Then modify the number of thumbnails in the ** theme config** by `thumbnail: random_amount`.

#### Isolation

This Scheme will only show thumbnails that have been customized.

## Create the About Me page

Create a new `about` page:

```shell
hexo new page "about"
```

If you want to add a link to the "Link" page, please refer to the [pages](/en/intro/#pages) .

## Create the "Links" page

### Create the page

Create a folder named `links` in the` source` folder under the hexo directory (just a suggestion, which you can modify as you like).

Then create a Markdown file named `index.md` in the file.

In the `index.md` file to write the following content.

```markdown
---
title: links
date:
layout: links
---
```

> `title` can be changed,` layout` can not be modified.

If you want to add a link to the "Link" page, please refer to the [pages](/en/intro/#pages).

### Add data

Also create a folder named `_data` (forbidden rename) within the` source` folder in the hexo directory.

And then create a file named `links.yml` in the file.

The format of a single link is:

```yaml
Name:
    link: http://example.com
    avatar: http://example.com/avatar.png
    descr: "This is a description"
```

> Add multiple links, just follow the above format can be repeated to fill.

- Change `Name` to the name of the link, eg ` Viosey`.
- `http://example.com` is the address of the friendly link.
- `http://example.com/avatar.png` is the link to the picture.
- `This is a description` for the link description.

## Create the "Gallery" page

### Create the page

Create a folder in the `source` folder under the hexo directory called` gallery` (just a suggestion, which you can modify as you like).

Then create a Markdown file named `index.md` in the file.

In the `index.md` file to write the following content.

```markdown
---
title: gallery
date:
layout: gallery
---
```

> `title` can be changed,` layout` can not be modified.

If you'd like to add an entry to the Gallery page, please refer to the separate [page](/en/intro/#pages).

### Add data

Also create a folder named `_data` (forbidden rename) within the` source` folder in the hexo directory.

Then create a file called `gallery.yml` in the file.

The format for a single image is:

```yaml
Name:
	full_link: http://example.com/full-image.png
	thumb_link: http://example.com/thumb-image.png
	descr: "This is a description"
```

> Add multiple pictures, just follow the above format can be repeated to complete.

- Change `Name` to the image name, for example` Material`.
- `http://example.com/full-image.png` is the full picture address.
- `http://example.com/thumb-image.png` is the address of the thumbnail image, if there is no thumbnail can also use the full picture of the address.
- `This is a description` for picture description.


## Create the "Tag Cloud" page

### Create the page

Create a folder in the `source` folder under the hexo directory called` tags` (just a suggestion, which you can modify as you like).

Then create a Markdown file named `index.md` in the file.

In the `index.md` file to write the following content.

```markdown
---
title: tags
date:
layout: tags
---
```

> `title` can be changed,` layout` can not be modified.

If you'd like to add an entry to the Gallery page, please refer to the separate [page](/en/intro/#pages).


## Create a private page

If an article does not want to appear in the site, just add it to the `front-matter`

```yaml
layout: private
```