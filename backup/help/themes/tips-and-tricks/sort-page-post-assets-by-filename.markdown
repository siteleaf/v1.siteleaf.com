---
title: Sort page/post assets by filename
date: 2014-06-27 14:40:00 Z
related_tag: sort
---

```liquid
{% assign sorted_assets = assets.all | sort:'filename' %}
<ol>
  {% for asset in sorted_assets %}
    <li>{{asset.url}}</li>
  {% endfor %}
</ol>
```
