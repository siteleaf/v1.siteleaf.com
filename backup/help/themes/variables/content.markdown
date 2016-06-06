---
title: Content
date: 2014-05-01 21:43:00 Z
---

Variable           | Description
--------           | -----------
`type`             | Can be `page`, `post`, `archive`, `taxonomy`, or `tag`.
`title`            | Title of content.
`url`              | URL to object without domain (e.g. `/blog/my-post`).
`permalink`        | Full URL to object with domain (e.g. `http://mysite.com/blog/my-post`).
`body`             | Body in HTML (rendered from Markdown), available in `page` and `post` types.
`body_raw`         | Body in raw Markdown, available in `page` and `post` types.
`excerpt`          | Shortened version of the body (use 2 empty lines to break), available in `page` and `post` types.
`excerpt_raw`      | Excerpt in raw Markdown, available in `page` and `post` types.
`assets`           | Array of [assets](#assets), available on `page` and `post` types.
`meta`             | Array of [metadata](#metadata), available on `page` and `post` types.
`taxonomy`         | Array of [taxonomy](#taxonomy), available on `post` type only.
`tags`             | Array of [tags](#tags), available on `taxonomy` type only.
`pages`            | Array of child-pages, available on `page` type only.
`posts`            | Array of posts, available in `page`, `archive`, and `tag` types.
`previous`         | The previous `page` or `post`, available in `page` or `post` types.
`next`             | The next `page` or `post`, available in `page` or `post` types.
`current`          | Alias of the curent `page` or `post`, available in `page` or `post` types.
`parent`           | Parent page object (if exists).
`archive_url`      | URL to archive page, available in `page` type only.
`date`             | Date of publish, available in `page` and `post` types.
`year`             | Year of publish (e.g. 2015)
`month`            | Numeric month of publish (e.g. 12)
`day`              | Numeric day of publish (e.g. 31)
`updated_at`       | Date of last update.
`author.fullname`  | Full name of author, available in `page` and `post` types.
`author.firstname` | First name of author, available in `page` and `post` types.
`author.lastname`  | Last name of author, available in `page` and `post` types.
`author.email`     | Author’s email, available in `page` and `post` types.
`author.avatar`    | Author’s Gravatar URL, available in `page` and `post` types.
`home?`            | Boolean if page is homepage, available in `page` type only.

Get the title and body for the current page:

```liquid
<h2>{{title}}</h2>

{{body}}
```

Check for parent page:

```liquid
{% if parent %}
  <a href="{{parent.url}}">&larr; Back to {{parent.title}}</a>
{% endif %}
```
