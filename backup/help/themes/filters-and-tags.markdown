---
title: Filters and tags
date: 2014-05-01 21:38:00 Z
related_tag: filters and tags
---

Siteleaf supports all [Standard Liquid Filters](https://github.com/Shopify/liquid/wiki/Liquid-for-Designers#standard-filters) and [Liquid Tags](https://github.com/Shopify/liquid/wiki/Liquid-for-Designers#tags).

Siteleaf is also compatible with [Jekyll Liquid Filters](http://jekyllrb.com/docs/templates/).

In addition, Siteleaf adds the following custom filters:

Filter             | Description                                                    | Example
--------           | -----------                                                    | -------
`fallback`         | Provide a default value if variable is blank.                  | {{title &#124; fallback:"Untitled"}}
`json`		   | Formats content as [JSON (JavaScript Object Notation)](http://en.wikipedia.org/wiki/JSON)  | {{site.posts &#124; json}}
`markdown`         | Converts [Markdown](http://daringfireball.net/projects/markdown/) to HTML, use `true` to apply Smartypants.  | {{title &#124; markdown:true}}
`smartypants`      | Applies [Smartypants](http://daringfireball.net/projects/smartypants/) (smart quotes, em/en dashes, etc).  | {{title &#124; smartypants}}
`slug`		   | Converts a string to its URL-friendly, slug form.			    | {{meta.custom_field &#124; slug}}
