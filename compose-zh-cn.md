---
title: 开始创作
version:
permalink: compose
id: 3
lang: zh-cn
---
## 创建文章

### 使用命令行
```shell
hexo new <title>
```

### 手动创建
在 hexo 主目录下 `source -> _posts` 新建以 `.md` 为后缀的文件。

### Front-matter

[Front-matter - 官方介绍](https://hexo.io/zh-cn/docs/front-matter.html)

| 参数          | 描述                | 默认值       |
|:--           |:--                  |:--           |
| `layout`     | 布局                | post         |
| `title`      | 标题                | 文件名       |
| `date`       | 建立日期            | 文件建立日期 |
| `updated`    | 更新日期            | 文件更新日期 |
| `tags`       | 标签（不适用于分页）|              |
| `categories` | 分类（不适用于分页）|              |
| `permalink`  | 覆盖文章网址        |              |
| `thumbnail`  | 缩略图地址          |              |
| `toc`        |  显示 TOC 按钮      | true        |
| `comment`      | 显示评论      | true        |
| `notag`      | 不生成标签按钮      | false        |

### 缩略图功能

在 Material 主题中，每个 Scheme 都有缩略图功能。
只需要在 `Front-matter` 中添加参数 `thumbnail: `，然后填入缩略图地址即可。

#### Paradox

此 Scheme 如果没有自定义缩略图，则使用默认随机缩略图，随机缩略图目录位于主题文件夹下 `source -> img -> random`。
随机缩略图可添加自己喜好的图片，格式为 `<num>.png` 。然后在 **主题配置文件** 中 `thumbnail:random_amount` 修改缩略图数量。

#### Isolation

此 Scheme 只会显示已自定义缩略图。


## 创建「关于我」页面

新建一个 `about` 页面：

```
hexo new page "about"
```

如果想添加「关于我」页面的入口，请参考 [独立页面](/intro/#pages)。

## 创建「友情链接」页面

### 创建页面
在 hexo 目录下的 `source` 文件夹内创建一个名为 `links`（只是建议，可根据自己喜好修改）的文件夹。

然后在文件内创建一个名为 `index.md` 的 Markdown 文件。

在 `index.md` 文件内写入如下内容即可。
```markdown
---
title: links
date: 
layout: links
---
```
>`title` 可修改，`layout` 不可修改。

如果想添加「友情链接」页面的入口，请参考 [独立页面](/intro/#pages)。

### 添加数据
同样在在 hexo 目录下的 `source` 文件夹内创建一个名为 `_data`（禁止改名）的文件夹。

然后在文件内创建一个名为 `links.yml` 的文件。

单个友情链接的格式为：

```yml
Name:
    link: http://example.com
    avatar: http://example.com/avatar.png
    descr: "这是一个描述"
```

>添加多个友情链接，只需要根据上面的格式重复填写即可。

- 将 `Name` 改为友情链接的名字，例如 `Viosey`。
- `http://example.com` 为友情链接的地址。
- `http://example.com/avatar.png` 为友情链接的头像。
- `这是一个描述` 为友情链接描述。


## 创建「图库」页面

### 创建页面
在 hexo 目录下的 `source` 文件夹内创建一个名为 `gallery`（只是建议，可根据自己喜好修改）的文件夹。

然后在文件内创建一个名为 `index.md` 的 Markdown 文件。

在 `index.md` 文件内写入如下内容即可。
```markdown
---
title: gallery
date: 
layout: gallery
---
```
>`title` 可修改，`layout` 不可修改。

如果想添加「图库」页面的入口，请参考 [独立页面](/intro/#pages)。

### 添加数据
同样在在 hexo 目录下的 `source` 文件夹内创建一个名为 `_data`（禁止改名）的文件夹。

然后在文件内创建一个名为 `gallery.yml` 的文件。

单个图片的格式为：

```yml
Name:
	full_link: http://example.com/full-image.png
	thumb_link: http://example.com/thumb-image.png
	descr: "这是一个描述"
```
>添加多张图片，只需要根据上面的格式重复填写即可。

- 将 `Name` 改为图片名字，例如 `Material`。
- `http://example.com/full-image.png` 为完整图片的地址。
- `http://example.com/thumb-image.png` 为图片缩略图的地址，如果没有缩略图也可使用完整图片的地址。
- `这是一个描述` 为图片描述。


## 创建「标签云」页面

### 创建页面

在 hexo 目录下的 `source` 文件夹内创建一个名为 `tags`（只是建议，可根据自己喜好修改）的文件夹。

然后在文件内创建一个名为 `index.md` 的 Markdown 文件。

在 `index.md` 文件内写入如下内容即可。
```markdown
---
title: tags
date: 
layout: tags
---
```
>`title` 可修改，`layout` 不可修改。

如果想添加「图库」页面的入口，请参考 [独立页面](/intro/#pages)。


## 创建「私有」页面
如果某篇文章不想显示在站点中，只需要在 `front-matter` 中加入
```yml
layout: private
```