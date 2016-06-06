---
title: Metadata
date: 2014-05-01 21:45:00 Z
related_tag: metadata
---

Metadata is pure key/value data attached to a site, page, post, or asset. It provides a way to interact with templates beyond the basic usage of injecting title or body copy. It could be a custom color value, location, an aside, anything.

Variable           | Description
--------           | -----------
`meta`             | Array of all metadata key/value pairs.
`meta.KEY`         | Get single metadata by key (ie. `Color`).

Available for each metadata:

Variable           | Description
--------           | -----------
`key`              | Name of metadata key (ie. `Color`).
`value`            | Value of metadata (ie. `Red`).

Count number of metadata fields:

```html
{{meta | size}}
```

Get metadata for key `Color`:

```liquid
{{meta.color}}
```

Get metadata for key `My Color`:

```liquid
{{meta['My Color']}}
```

Loop through metadata:

```liquid
<dl>
{% for data in meta %}
  <dt>{{data.key}}</dt> <dd>{{data.value}}</dd>
{% endfor %}
</dl>
```

Conditional for specific metadata value:

```liquid
{% if meta.color.value == 'Red' %}
  <p>This color is red!</p>
{% endif %}
```

Get posts by metadata value:

```liquid
{% assign sticky_posts = site.posts | where:"meta.sticky","yes" %}
```
