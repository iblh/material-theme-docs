# Compose

## Create an article

### Use the command line

```bash
hexo new <title>
```

### Create it manually

Create a file with the extension `.md` inside the `source/_posts` folder.

## Front-matter

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
| mathjax        | Enable the MathJax for this post     | false             |

P.S. To use `Pin on top` feature please visit [topPost](/intro/#topPost)

## Thumbnail function

In the Material theme, each Scheme has a thumbnail function. Simply add the `thumbnail:` parameter to the `front-matter` and fill in the thumbnail address.

### Paradox

This scheme uses the default random thumbnails if there is no custom thumbnail. The random thumbnail directory is located under the `source/img/random` folder. You can add your favorite images in the format `material-<num>.png`. Then modify the `random_amount` parameter in the **theme config**.

### Isolation

This Scheme will only show thumbnails that have been customized.

If you want to add a link to the "Link" page, please refer to the [page settings](/en/intro/#pages).
