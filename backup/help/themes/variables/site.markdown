---
title: Site
date: 2014-05-01 21:42:00 Z
---

`site` contains global variables available to all pages.

Variable           | Description
--------           | -----------
`site.title`       | The title of your website.
`site.domain`      | Your website’s domain name (ie. `barlawrence.com`).
`site.permalink`   | Your website’s full address (ie. `http://barlawrence.com`).
`site.pages`       | A nested array of pages.
`site.posts`       | Array of all posts in all pages.
`site.feed_url`    | URL to your website’s [RSS](http://en.wikipedia.org/wiki/RSS) feed (ie. `http://barlawrence.com/feed.xml`).
`site.sitemap_url` | URL to your website’s [Sitemap](http://www.sitemaps.org) file (ie. `http://barlawrence.com/sitemap.xml`).
`site.date`        | Date of most recent publish.

For example, use the following Liquid to get the title of your website:

```liquid
{{site.title}}
```

Loop through `site.pages` to build a menu:

```liquid
<nav>
  <ul>
  {% for page in site.pages %}
    <li><a href="{{page.url}}"{% if page.url == url %} class="selected"{% endif %}>{{page.title}}</a></li>
  {% endfor %}
  </ul>
</nav>
```
