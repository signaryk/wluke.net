---
layout: post
title: Adventures in OpenBSD 
date: 2020-02-11
---
## Introduction
Last week I decided to set up a new remote development server. I wanted to use this to host some web pages, Git
repos for my personal projects, and my personal IRC gateway. Originally I had planned to use Debian, but as I was
getting ready to provision the server, I stumbled upon the [Tildeverse](https://tildeverse.org) project. A few of
the participating "tilde" servers ran on OpenBSD, so I decided to do some digging into the OpenBSD project. 

I was pretty impressed with the amount of documentation for their operating system. The 
[manpages](https://man.openbsd.org) were pretty straightforward to read through and the examples were very helpful 
in working through issues, especially with configuration files. I was also impressed with the project's core values
of secure, clean, and maintainable code. At any rate, I was intrigued enough to choose OpenBSD as the operating
system for my server and, and decided to use this as an opportunity to learn another platform.

## Setting Up `httpd`
After provisioning, the first thing I set about configuring was OpenBSD's native webserver, `httpd`. Created as a
replacedment to Apache or nginx, httpd serves to be an HTTP server written in line with OpenBSD's goals and
philosophies. Writing the configuration file is  
