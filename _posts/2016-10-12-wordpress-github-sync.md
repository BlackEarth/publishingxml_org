---
ID: 27
post_title: WordPress GitHub Sync
author: sah
post_date: 2016-10-12 10:08:36
post_excerpt: ""
layout: post
permalink: >
  http://publishingxml.org/2016/10/12/wordpress-github-sync/
published: true
---
WordPress is a great package for hosting a website, but out-of-the-box it has limitations for use as a community project hub. One of those limitations occurred to me while I was setting all this up last night: _What if I want people to contribute to the website as to the project in general, by forking a github repository and making pull requests? It would really be nice to be able to sync a WordPress site with a github repository._

It turns out that WordPress has a plugin for that: [WordPress GitHub Sync](https://wordpress.org/plugins/wp-github-sync/). Very easy to set up, took about 15 minutes, including learning how to do it from the documentation.

So now, [publishingxml.org](http://publishingxml.org) (this site) is syncing its posts and pages with the [publishingxml.org github repository](https://github.com/BlackEarth/publishingxml_org). Anyone can fork that repository and submit pull requests; accepted pull requests will be published to the website. Very cool.

(In fact, I wrote this post on my desktop and pushed it to github, and voila, it was published.)

At first I set up the sync with the main publishing-xml repository, which does make some sense: After all, [publishingxml.org](http://publishingxml.org) is going to hold the documentation for the Publishing XML project, and shouldn't that documentation also be in the main repository? Yes, probably, but the website is going to hold a lot more than documentation, and we don’t necessarily want everything that we do on the website to be in the main repository (such as this post). So, a separate repository, making the website a separate subproject. (We’re already up to three repositories, and I haven't even invited other contributors yet.)

The documentation question is bugging me, though. What makes sense is to write the documentation for Publishing XML in the main [publishing-xml repository](https://github.com/BlackEarth/publishing-xml), and then to set up some kind of process by which to update the documentation on the website. Such as, whenever making a release of publishing-xml itself, push the updated documentation to the website.