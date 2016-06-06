---
title: Group and exclude posts
date: 2014-06-27 14:57:00 Z
related_tag: group
---

```liquid
{% assign featured_ids = '' %}
 
Featured:

{% for post in taxonomy['tags']['featured'].posts limit:4 %}
  {% assign featured_ids = featured_ids | append:',' | append:post.id %}
  <article class="featured">{{post.title}}</article>
{% endfor %}
 
Everything else:

{% for post in posts %}
  {% unless featured_ids contains post.id %}
    <article class="normal">{{post.title}}</article>
  {% endunless %}
{% endfor %}
```
