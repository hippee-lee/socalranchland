---
id: 5296
title: grunt_and_deploy
date: 2013-08-09T10:16:38+00:00
author: matth
layout: post
guid: http://hippeelee.com/blog/?p=5292
permalink: /2013/08/09/grunt_and_deploy/
categories:
  - (intro)Spection
---
This is about tools. Not the scary old dude at the Katie Perry concert by himself or the harmoniously awesome band. My tools. The same ones you might use if you decide to make something similar things that interest me.

See, about a year ago I started down a new path. I thought it was the same old path I had ridden a thousand times before. But it wasn&#8217;t. It was different. The opportunity was different and I knew that by the time the interview ended and they had had good, thoughtful answers for most of my questions. <!--more-->

And then, they didn&#8217;t even want me to do traditional web development. Well they did but the iOS stuff was more important, they were agile and I was the one who had drunk the most from Apple&#8217;s cool aid jar. Never mind you that I only had half way completed the Stanford iOS series and gotten busy with the move back to the west coast. Never mind that I really didn&#8217;t understand what a delegate pattern was or how to implement it in Objective-C or any language. They were agile. I was interested; and I was smart enough from wondering what was wrong with the folks I was trying to learn from while stumbling around various Boulder *start-up&#8217;s (1) who claimed to be agilely implementing the next great OOP architected LAMP CRUD web app with an iframed UIWebView container for the website as a native version for iOS.

I digress, this is about tools. But the stumbling and internal questioning I did was integral in figuring out just how important your tools are. See, I already knew about tools in the real world. [Dad taught me that.](http://hippeelee.com/blog/2012/02/an-easy-toolchain/ "An Easy Toolchain")So, when I got the opportunity to dive into Xcode and build compiled software I spent some time learning how to debug with gdb first and the lldb when they switch it over. Break points, stack traces and Instruments. Oh my! What an eye opener after working in php log dumps for so long. Then I also had to get into the CI side of things for some stuff and now for the api our Angular app runs on and PHPStorm was the right tool for the job.

So I was using these new (to me) tools and getting more productive. Now I am incorporating SublimeText into the flow as a pseudo replacement for emacs across all platforms. I can version control the config file, drop it onto my Ubuntu dev server, windows VM and MBP development laptop and have the same editor with a quick git pull from my bitbucket. The whole point of this post is to highlight the power of tools and for the first time in a long time not only am I using others but I am creating my own.

SInce moving back to front end implementation and the Angular app I have discovered the tool chain associated with efficiently writing code and seeing the results. It&#8217;s not instantaneous but it&#8217;s a lot faster than when I started my second career and this whole software thing. So, in solving my issue (how to use grunt to develop for IE I wrote a quick script to compile and deploy the app to my dev server. I call it, appropriately grunt\_and\_deploy.

&nbsp;

(1) IMO 90% of Boulder start-ups are really lifestyle businesses in disguise.