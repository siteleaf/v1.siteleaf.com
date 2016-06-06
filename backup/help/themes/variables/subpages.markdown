---
title: Subpages
date: 2014-05-01 21:45:00 Z
---

See [Content](/help/themes/variables/content) for available variables.

Count the number of subpages:

```liquid
This page has {{pages | size}} subpages.
```

Loop through the subpages:

```liquid
{% for page in pages %}
<article>
  <h3><a href="{{page.url}}">{{page.title}}</a></h3>
  {{page.body}}
</article>
{% endfor %}
```
