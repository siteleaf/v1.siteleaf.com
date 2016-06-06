---
title: Assets
date: 2014-05-01 21:45:00 Z
related_tag: assets
---

Variable           | Description
--------           | -----------
`type`             | Can be `image`, `audio`, `video`, or `other`.
`filename`         | Name of file (ie. `photo.jpg`).
`url`              | URL to object without domain (ie. `/assets/photo.jpg`).
`permalink`        | Full URL to object with domain (ie. `http://mysite.com/assets/photo.jpg`).
`content_type`     | MIME type of asset (ie. `image/jpeg`).
`filesize`         | Size of file in bytes (ie. `1024`).
`date`             | Date asset was created.

Count the number of assets:

```liquid
{{assets | size}}
```

Loop through assets:

```liquid
{% for asset in assets %}
  {% if asset.type == 'image' %}
    <img src="{{asset.url}}">
  {% elsif asset.type == 'audio' %}
    <audio><source src="{{asset.url}}" type="{{asset.content_type}}"></audio>
  {% elsif asset.type == 'video' %}
    <video><source src="{{asset.url}}" type="{{asset.content_type}}"></video>
  {% elsif asset.type == 'other' %}
    <a href="{{asset.url}}">Download {{asset.filename}}</a></li>
  {% endif %}
{% endfor %}
```
