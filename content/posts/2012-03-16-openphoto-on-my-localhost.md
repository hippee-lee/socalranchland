---
id: 4584
title: Openphoto On My Localhost
date: 2012-03-16T10:05:55+00:00
author: matth
layout: post
guid: http://hippeelee.com/blog/?p=4584
permalink: /2012/03/16/openphoto-on-my-localhost/
categories:
  - (intro)Spection
---
I set up [The Openphoto Project](http://theopenphotoproject.org/) on my localhost this morning and kept a few notes:

You don&#8217;t need to have aws accounts, you can use the file system but you don&#8217;t know this until you start going through the site setup after the software, db and web server are nicely talking. In my case I got an answer on the irc channel.

Once I got the software, db and webserver configured and running I navigated through the setup steps and ran into the following:

I was getting an

> &#8220;Insufficient privileges to complete setup&#8221;

message that says to make sure my user can write to:

> /your/path/to/frontend/src/userdata.

However I didn&#8217;t see a userdata folder in

> /path/to/frontend/src/

My user did own the frontend folder and everything below it and I almost went to irc to ask for advice. As I was typing out my question it occurred to me to manually make the directory myself and reload the page, who knows right?

> $ mkdir userdata

Lo and behold, it worked. Awesome. Lets continue. After a bit of irc advice to change MAMP&#8217;s MySQL port to 3306 &#8211; I got through the configuration steps and added some photo&#8217;s. Yay!