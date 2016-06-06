---
title: Sort and loop through all tags
date: 2014-06-27 14:41:00 Z
related_tag: sort
---

```liquid
{% assign sorted_tags = site.pages['blog'].taxonomy['tags'] | sort:'value' %}
<ul>
    {% for tag in sorted_tags %}
    <li><a href="{{tag.url}}">{{tag.value}}</a></li>
    {% endfor %}
</ul>
```

Swap `blog` for your page's slug, and `tags` for the name of your tagset (if not using the default tags).
