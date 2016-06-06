---
title: Taxonomy and Tags
date: 2014-05-01 21:46:00 Z
related_tag: taxonomy
---

Siteleaf allows you to use multiple tag sets called Taxonomy. By default, each site will have one set called `Tags`.

Variable           | Description
--------           | -----------
`taxonomy`         | Array of all taxonomy sets.
`taxonomy.KEY`     | Get tags by set name, ie. `Tags`.

### Taxonomy:

Variable           | Description
--------           | -----------
`key`              | Name of taxonomy set, ie. `Tags`.
`slug`             | URI slug for set, ie. `tags`.
`url`              | URL for set page without domain, ie. `/blog/tags`
`permalink`        | URL for set page with domain, ie. `http://mysite.com/blog/tags`
`tags`             | Array of [tags](#tags) in set.
`tags.KEY`         | Get single tag by name, ie. `Design`.

### Tags:

Variable           | Description
--------           | -----------
`value`            | Name of tag, ie. `Design`.
`slug`             | URI slug for tag set, ie. `design`.
`url`              | URL for tag page without domain, ie. `/blog/tags/design`
`permalink`        | URL for tag page with domain, ie. `http://mysite.com/blog/tags/design`
`posts`            | Array of [posts](#posts) with this tag.

Count number of tags in the default `Tags` set:

```liquid
{{taxonomy['tags'] | size}}
```

Count number of tags in the `Colors` tag set:

```liquid
{{taxonomy['colors'] | size}}
```

Get first tag in the `Colors` tag set:

```liquid
{{taxonomy['colors'].first}}
```

Loop through the `Tags` set:

```liquid
<ul>
{% for tag in taxonomy['tags'] %}
  <li><a href="{{tag.url}}">{{tag.value}}</a></li>
{% endfor %}
</ul>
```

Loop through the `Colors` set:

```liquid
<ul>
{% for tag in taxonomy['colors'] %}
  <li><a href="{{tag.url}}">{{tag.value}}</a></li>
{% endfor %}
</ul>
```

Loop through all tag sets:

```liquid
<ul>
{% for set in taxonomy %}
  <li>{{set.key}} ({{set | size}} tags)
    <ul>
    {% for tag in set %}
      <li><a href="{{tag.url}}">{{tag.value}}</a></li>
    {% endfor %}
    </ul>
  </li>
{% endfor %}
</ul>
```

Loop through the `Food` set on the `Blog` page, then display all posts for each tag:

```liquid
{% for tag in site.pages.blog.taxonomy['Food'] %}
  <h1>{{ tag.value }}</h1>

  {% for post in tag.posts %}
    <a href="{{ post.url }}">{{ post.title }}</a>
  {% endfor %}
{% endfor %}
```
