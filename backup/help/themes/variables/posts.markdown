---
title: Posts
date: 2014-05-01 21:43:00 Z
---

See [Content](/help/themes/variables/content) for available variables.

Posts belong to a page. A post could be a blog post, a portfolio item, an event, or anything that makes sense ordered chronologically. Posts are very similar to a Page, however they can have taxonomies and are ordered chronologically by default.

Count the number of posts:

```liquid
This page has {{posts | size}} posts.
```

Loop through the first 20 posts on the current page:

```liquid
{% for post in posts limit:20 %}
<article>
  <header><a href="{{post.url}}">{{post.title}}</a></header>
  {{post.body}}
  <footer>Posted on {{post.date | date: "%b %d, %Y"}} by {{post.author.fullname}}</footer>
</article>
{% endfor %}
```

Loop through all posts where the author is Sawyer:

```liquid
{% assign my_posts = site.posts | where:"author","Sawyer" %}

<ul>
  {% for post in my_posts %}
    <li><a href="{{post.url}}">{{post.title}}</a></li>
  {% endfor %}
</ul>
```
