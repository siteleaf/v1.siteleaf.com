---
title: Getting started
date: 2014-05-01 21:17:00 Z
related_tag: getting started
---

Siteleaf uses the popular [Liquid](https://github.com/Shopify/liquid) syntax for themes. If you can write HTML, you’ll have no problem using Liquid.

Here’s how a simple template might look:

```liquid
<html>
<head>
	<title>{{site.title}} | {{title}}</title>
</head>
<body>

  <h1>{{title}}</h1>

  <article>{{body}}</article>

  {% if parent %}
  <p><a href="{{parent.url}}">&larr; Go back</a></p>
  {% endif %}

</body>
</html>
```

As you can see, there are two types of markup in Liquid:

1) Output markup (which may resolve to text) is surrounded by
```liquid
{{ matched pairs of curly brackets (ie, braces) }}
```

2) Tag markup (which cannot resolve to text) is surrounded by
```liquid
{% matched pairs of curly brackets and percent signs %}
```

If you are new to the Liquid syntax, a good place to start is [Liquid for Designers](https://github.com/Shopify/liquid/wiki/Liquid-for-Designers).
