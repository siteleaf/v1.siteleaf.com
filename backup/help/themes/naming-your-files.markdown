---
title: Naming your files
date: 2014-05-01 21:47:00 Z
related_tag: naming your files
---

Siteleaf themes may contain one or more templates.

Your base template should always be called `default.html`.

Additional templates can be applied to other pages by following the same URL structure as your website:

URL               | Template
---               | --------
*                 | default.html (required, used by default)
/                 | index.html
/blog             | blog.html (or blog/index.html)
/blog/new-post    | blog/default.html (default template for 'blog' posts)
/blog/custom-post | blog/custom-post.html (template only applied to this page)
/blog/archive     | blog/archive.html (or blog/archive/index.html)
