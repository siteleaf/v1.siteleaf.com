---
title: Includes / Partials
date: 2014-05-01 21:47:00 Z
related_tag: includes
---

Includes (or partials) can be added by using the `include` tag:

```liquid
{% include 'header' %}

{% include 'includes/menu' %}
```

Include files should be prepended with an underscore. In the above examples, Siteleaf will look for `_header.html` and `_includes/menu.html` respectively.
