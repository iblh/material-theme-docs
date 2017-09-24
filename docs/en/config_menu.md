# Menu Settings

## toc

Choose whether the line_number of toc(Table of Content) will show or not. Available value of "linenumber": true | false

## sns

Used to fill in your SNS information. Except for `email` (which is displayed in the sidebar), a specific icon will be put inside the footer for each url you put.

- `email`
- `facebook`
- `twitter`
- `googleplus`
- `weibo`
- `instagram`
- `tumblr`
- `github`
- `linkedin`
- `zhihu`
- `bilibili`
- `telegram`

## sns_share

Used to choose which items will be displayed in share menu.

- `twitter`
- `facebook`
- `googleplus`
- `weibo`
- `linkedin`
- `qq`
- `telegram`

## sidebar

### dropdown

Used to set the Paradox sidebar drop-down menu (empty by default).

Refer to the configuration style

```yaml
dropdown:
    Email Me:
    link: "#"
    icon: email
```

### homepage

Used to set the home page button.

- `use`: set `true` to display this button is the sidebar
- `icon`: add an Material Design icon before the name of the button. Let it empty for no icon.
- `divider`: set `true` to add a divider after the button

### archives

Used to set the archives button.

- `use`: set `true` to display this button is the sidebar
- `icon`: add an Material Design icon before the name of the button. Let it empty for no icon.
- `divider`: set `true` to add a divider after the button

### categories

Used to set the categories button.

- `use`: set `true` to display this button is the sidebar
- `icon`: add an Material Design icon before the name of the button. Let it empty for no icon.
- `divider`: set `true` to add a divider after the button

### pages

Used to set up custom pages (empty by default). The pages will appear in the sidebar.

Refer to the configuration style. Let the icon empty if you don't need one. Set `true` to divider if you want a divider after the page button.

```yaml
pages:
    About:
        link: "#about"
        icon: person
        divider: false
    timeline archive:
        link: "/timeline/"
        icon:
        divider: false
```

### article_num

Used to display the number of articles.

- `use`: set `true` to display this button is the sidebar
- `divider`: set `true` to add a divider after the button

### footer

Used to customize the sidebar footer.

- `divider`: set `true` to add a divider before the footer
- `theme`: set `true` to display a link to the theme site
