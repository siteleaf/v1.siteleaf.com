---
title: GitHub Pages
date: 2014-05-27 22:58:00 Z
---

Siteleaf now supports publishing to [GitHub Pages](https://pages.github.com).

### Benefits
GitHub Pages is a solid choice for static web hosting, especially if you already use [GitHub](http://github.com) to manage your theme code. 

It's [fast](http://www.jeremymorgan.com/blog/programming/how-fast-are-github-pages/), [CDN-backed](http://www.fastly.com/customers/github/), and the best part: it's fully version-controlled, allowing you to see a commit log of all publishes and revert to previous publish states.

### How it works
To use GitHub hosting, jump to your site's Settings page in Siteleaf. From there, you can choose GitHub Pages and authenticate with your GitHub account. Next, choose the repository you'd like to publish to (this should have the format: `username/repository`).

If you are familiar with GitHub Pages, we use what is known as [Project Pages](https://help.github.com/articles/user-organization-and-project-pages#project-pages) which use a `gh-pages` branch in your repo (as opposed to User or Organization Pages). This allows you to retain your theme assets in the same repo's `master` branch (optional). Siteleaf will create the `gh-pages` branch for you if it doesn't already exist.

Siteleaf will also create a [CNAME file](https://help.github.com/articles/setting-up-a-custom-domain-with-github-pages) for your domain as set in your Siteleaf Settings, so please ensure this is correct (including `www.` as necessary).

If using a custom domain, your CNAME record should point to `username.github.io`.

### Security
Siteleaf connects to GitHub's API using OAuth, and will only make changes in your chosen repo's `gh-pages` branch. 

In the case where your account has access to multiple repositories (and security is a concern), we recommend setting up a [Machine User](https://help.github.com/articles/managing-deploy-keys#machine-users) which only has access to the required repo(s) for Siteleaf.

Once authorized, you can revoke Siteleaf's API access from your [GitHub account](https://github.com/settings/applications) at any time.

### Limitations
Since Siteleaf uses Project Pages, your repo should be named anything other than `username.github.io` which is reserved for User/Organization Pages. Initial setup and domain name changes can take up to 10 minutes for GitHub to resolve. Once set up, content changes will appear almost instantly after publish.

GitHub's API currently supports a maximum size of around 15 MB per file. If you need to host larger files (like videos or zip files), you can upload these manually using Git or host them on an external service like YouTube or Dropbox.

When creating new repositories, an initial commit is required before Siteleaf is able to publish. If your repo is completely blank, the easiest way to get started is to add a simple [README file](https://help.github.com/articles/create-a-repo) using GitHub.com.

### More
To learn more about GitHub Pages see: https://help.github.com/categories/20/articles
