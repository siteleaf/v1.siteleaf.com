---
title: Using Markdown in metadata
date: 2013-10-29 15:55:00 Z
assets:
- path: "/uploads/meta-markdown.png"
tags:
- tip
- markdown
- liquid
Docs:
- metadata
---

In previous posts, we talked about using [Markdown](http://www.siteleaf.com/blog/markdown-in-siteleaf/) for text formatting and [Metadata](http://www.siteleaf.com/blog/metadata-in-siteleaf/) for extending your content in Siteleaf.

Markdown makes it easy to add links and `*emphasis*` to your content without having to write HTML. While your `body` content uses Markdown by default, you can also apply this easy-to-use formatting to your metadata.




Just add Markdown right in your metadata field:

![meta-markdown](/uploads/meta-markdown.png) 

Then in your template, apply the [markdown](https://github.com/siteleaf/siteleaf-themes#filters-and-tags) Liquid filter:

```
{{site.meta['sidebar'] | markdown}}
```

That's it!

You can use this to add links and simple markup to sidebar text, footers, post summaries, and anywhere else you use metadata.
