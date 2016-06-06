---
title: Redirects
date: 2014-07-15 16:13:00 Z
---

Here's a simple way to redirect any page or post in Siteleaf. First, add this to your template's HTML `<head>`:

```liquid
<head>
{% if meta.redirect %}
  <meta http-equiv="refresh" content="0;url={{meta.redirect}}">
{% endif %}
</head>
```

Then create a `redirect` metadata field on your page or post, with the value set to your destination URL.

If using external hosting, you can also set up 301 redirects manually using [Amazon S3](http://docs.aws.amazon.com/AmazonS3/latest/dev/how-to-page-redirect.html) or an [htaccess](http://css-tricks.com/snippets/htaccess/301-redirects/) file on your S/FTP server. Google is able to understand both 301 redirects and [meta refresh](https://support.google.com/webmasters/answer/79812?hl=en).
