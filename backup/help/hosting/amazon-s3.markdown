---
title: Amazon S3
date: 2014-06-04 01:28:00 Z
---

Siteleaf supports publishing to Amazon's [Simple Storage Service](http://aws.amazon.com/s3/). S3 is a low-cost, highly durable service for static file storage and websites. 

### Benefits
S3 allows you to set up [custom redirects and routing rules](http://docs.aws.amazon.com/AmazonS3/latest/dev/HowDoIWebsiteConfiguration.html).

AWS currently offers a Free Tier which includes 5GB storage and 20,000 hits per month in your first year, for more see: http://aws.amazon.com/free/

### Limitations
Amazon S3 is not a content delivery network, meaning your files will be served from a single data center. If you have a large amount of world-wide traffic, you may want to serve your S3 content through a CDN like [Amazon CloudFront](https://aws.amazon.com/cloudfront/).
