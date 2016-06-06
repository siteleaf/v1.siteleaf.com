---
title: Strip linebreaks from HTML
date: 2014-06-27 14:50:00 Z
---

```liquid
{% capture html %}
<html>
...
</html>
{% endcapture %}{{ html | strip_newlines }}
```
