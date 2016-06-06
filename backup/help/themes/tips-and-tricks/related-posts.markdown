---
title: Related posts
date: 2014-06-27 15:22:00 Z
related_tag: where
---

Show other posts with similar tags as the current post:

```liquid
<ul>
{% for related_post in parent.posts %}
  {% for tag in current.taxonomy['tags'].values %}
    {% if related_post.taxonomy['tags'][tag.slug] and related_post.id != current.id %}
      <li><a href="{{related_post.url}}">{{related_post.title}}</a></li>
      {% break %}
    {% endif %}
  {% endfor %}
  {% if forloop.index == 3 %}{% break %}{% endif %}
{% endfor %}
</ul>
```
