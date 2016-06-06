---
title: Content from other pages
date: 2015-04-16 22:06:00 Z
---

To access [variables](/help/themes/variables/content/) from a specific page on your site, you can reference it using its slug: `site.pages['your-slug']`

For example, we could grab the title and body from our `/about` page and re-use it somewhere else in our site:

```liquid
{% assign about_page = site.pages['about'] %}

<h2>{{ about_page.title }}</h2>
{{ about_page.body }}
```

Here's a quick shorthand version if you only need to access a single variable:

```liquid
{{ site.pages['about'].body }}
```

### Subpages

You can also reference nested pages:

- `site.pages['about'].pages` - gets all nested pages under `/about/*`
- `site.pages['about'].pages['team']` - gets the nested page `/about/team`

### Posts

Posts can be accessed in a similar way, using `posts` instead of `pages`:

- `site.posts['hello-world']` - looks for post in any page `/*/hello-world`
- `site.pages['blog'].posts` - gets all blog posts under `/blog/*`
- `site.pages['blog'].posts['hello-world']` - gets the post `/blog/hello-world`
- `site.pages['blog'].taxonomy['tags']['featured'].posts` - gets posts tagged "featured"

### Relative content

For flexibility in your theme you can reference content relative to the current page:

- `pages['your-slug']` - gets child page under current page
- `parent.pages` - gets all sibling pages from parent page
- `parent.pages['your-slug']` - gets sibling from parent page

The same can be applied to posts. For example, `parent.posts` would get all sibling posts.
