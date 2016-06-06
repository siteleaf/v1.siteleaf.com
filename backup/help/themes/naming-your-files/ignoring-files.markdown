---
title: Ignoring files
date: 2014-05-15 16:12:00 Z
---

To tell Siteleaf to ignore a certain file or directory when uploading your theme, add a `.siteleafignore` file to your theme folder. Within this file you can create a list of rules for ignoring files. This file is very similar to a `.gitignore` file and follows the same structure. [You can read more about that here.](http://git-scm.com/docs/gitignore)

Here's an example of a .siteleafignore file:

```
.DS_Store
.sass-cache
.git
bower_components
scripts/coffee/*.*
styles/sass/*.*
config/*.*
Gemfile
Guardfile
Gemfile.lock
```
