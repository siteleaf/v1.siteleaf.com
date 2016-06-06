---
title: Standalone templates
date: 2015-03-11 20:26:00 Z
---

If you want to use Liquid within other files (such as `feed.xml` or `pages.json`), just create the file as you normally would, but append `.liquid` to the filename. 

For example, if you wanted to create a JSON file with all of your blog posts, you would create a `blog.json.liquid` file (the filename can be whatever you like). Within this file you could use the `json` [Liquid filter](/help/themes/filters-and-tags/) to properly format your posts in JSON. When you publish your Siteleaf site, a `blog.json` file is automatically created for you.
