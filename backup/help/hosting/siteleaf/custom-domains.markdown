---
title: Using custom domains with Siteleaf Hosting
date: 2014-05-12 14:23:00 Z
assets:
- path: "/uploads/domain-settings.png"
---

To use your own domain with Siteleaf Hosting (e.g. `www.example.com`), check the "Use custom domain" option under your site's settings. 

![Domain settings](/uploads/domain-settings.png) 

After you save your changes, Siteleaf will display an address above the domain field. This address is the unique CDN address for your site.

#### Subdomains

To use a custom subdomain (e.g. `blog.example.com`), create a CNAME record in your domain provider's DNS settings. This should point to your unique CDN address.

| Record | Name | Target |
|--------|------|--------|
| `CNAME`  | `blog`  | `abc123.rackcdn.com` |

#### Root domains

Since CNAME records are not generally supported on root domains (e.g. `example.com`), you will need to redirect your root domain to a subdomain (generally `www`). In your domain provider's DNS settings, follow these settings:

1. Redirect your root domain to its www version (e.g. `www.example.com`). 

2. Edit the CNAME for `www` and point it to your unique CDN address.

| Record | Name | Target |
|--------|------|--------|
| `URL` or `Forward` | `@` or `example.com` | `www.example.com` |
| `CNAME`  | `www`  | `abc123.rackcdn.com` |

Note: If your domain provider does not support redirects (sometimes called URL records), you can use the free service wwwizer: http://wwwizer.com/naked-domain-redirect
