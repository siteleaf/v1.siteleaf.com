---
title: Rackspace Cloud Files
date: 2014-06-04 01:28:00 Z
---

Siteleaf supports publishing to [Rackspace Cloud Files](http://www.rackspace.com/cloud/files/).

### Benefits
Cloud Files is powered by Akamai CDN with over 200 global edge locations around the world.

### Limitations
Published changes can take up to 15 minutes to propogate throughout the Cloud Files CDN. 

Custom domains must use a `CNAME` record (not an `A` record), this typically means using a subdomain like `www.example.com` instead of `example.com`. For more, see [using custom domains](/help/hosting/siteleaf/custom-domains).
