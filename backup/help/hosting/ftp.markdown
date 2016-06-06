---
title: FTP and SFTP
date: 2014-06-04 01:28:00 Z
assets:
- path: "/uploads/sftp.png"
---

Siteleaf allows you to publish to any web host that supports standard [FTP](http://en.wikipedia.org/wiki/File_Transfer_Protocol) or [SFTP](http://en.wikipedia.org/wiki/SSH_File_Transfer_Protocol) (also known as Secure or SSH File Transfer Protocol). 

These hosts include:
- [Media Temple](http://mediatemple.net)
- [DreamHost](http://www.dreamhost.com)
- [1&1](http://www.1and1.com)
- [Bluehost](http://www.bluehost.com)
- [GoDaddy](http://www.godaddy.com)
- [HostGator](http://www.hostgator.com)
- and more

### Settings

![SFTP settings](/uploads/sftp.png) 

### Benefits

Publishing to your own FTP or SFTP server gives you full control over your files, and (depending on your web host) the ability to use `.htaccess` files to set up [301 redirects](http://css-tricks.com/snippets/htaccess/301-redirects/) or [password protect](http://css-tricks.com/easily-password-protect-a-website-or-subdirectory/) your published content.

### Limitations

Siteleaf currently supports the FTP and SFTP protocols only, not [FTPS](http://en.wikipedia.org/wiki/FTPS).

Siteleaf subdomains (e.g. `yourname.siteleaf.net`) are not supported with FTP or SFTP hosting.
