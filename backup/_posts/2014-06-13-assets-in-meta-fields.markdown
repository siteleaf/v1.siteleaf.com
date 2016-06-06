---
title: 'Quick tip: Assets in meta fields'
date: 2014-06-13 14:22:00 Z
hero: 
assets:
- path: "/uploads/pdf.gif"
tags:
- tip
- liquid
---

![](/uploads/pdf.gif) 

Siteleaf makes it easy to assign assets in your metadata fields, just drag and drop (as shown above).

Now in your theme, you can easily link to your asset:

```
<a href="{{ meta['project_link'] }}">
  {{ meta['project_link_title'] }}
</a>
```

This is a great way to reference special assets like featured images or PDF downloads.

To learn more about metadata see our tutorial [Metadata in Siteleaf](/blog/metadata-in-siteleaf).
