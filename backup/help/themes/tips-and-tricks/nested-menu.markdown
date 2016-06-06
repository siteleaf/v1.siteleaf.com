---
title: Nested menu
date: 2014-06-27 14:38:00 Z
---

```liquid
<ul>
  {% for page in site.pages %}
  <li>
    <a href="{{page.url}}"{% if page.url == url %} class="is-current-page"{% endif %}>{{page.title}}</a>
    {% if page.pages.size > 0 %}
    <ul>
      {% for subpage in page.pages %}
        <li>
          <a href="{{subpage.url}}"{% if subpage.url == url %} class="is-current-page"{% endif %}>{{subpage.title}}</a>
        </li>
      {% endfor %}
    </ul>
    {% endif %}
  </li>
  {% endfor %}
</ul>
```
