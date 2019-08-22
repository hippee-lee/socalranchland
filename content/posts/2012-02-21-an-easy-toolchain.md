---
id: 3090
title: An Easy Toolchain
date: 2012-02-21T09:16:40+00:00
author: matth
layout: post
guid: http://hippeelee.com/blog/?p=3090
permalink: /2012/02/21/an-easy-toolchain/
categories:
  - Computing
  - Dad
tags:
  - Memories
  - troubleshooting
---
I learned about tools from my dad. He used to fix everything us kiddos broke around the house and the cars and other engine driven things we used. I remember he had a method that included starting from the problem and working backwards through the solution. I spent alot of time bored out of my mind, holding his tools. Sometimes I was sent to get different tools but usually he brought a couple of different general purpose tools and was able to make due with them.

Its funny, the more I learn about software and software development, even from a web slanted view, it all depends on the tools you use. It depends on the tools that work best with your style. I have been keeping my personal projects and org-mode files under version control at bitbucket with mercurial for a few years now and while not completely immersed in the distributed version control environment, I am drawn to the benefits of it. Namely being able to commit to my repo whenever and whereever I am internt access or no internet access.

As I ramp up the search for opportunities in the next phase there are a lot of things I still need<!--more--> to process but publishing my resume online, branded as me and independent of everything else is the most important thing I need to maintain right now. I have very specific requirements and even more functionality that I am going to add so it makes sense to put it under version control, even if it only starts out at html/css/JavaScript. Since bluehost already has git installed for me to use and, fortuitously, since bitbucket started offering git as an option when creating a new repository, I put the first version in there.

The past few days I have gotten it to the point where I am comfortable publishing it and sending out some requests for feedback on the content and behavior of the layout. You know how it is though, especially with projects that are personal: you always find little things that need tweaked. I found the ease of deployment for a static html site super easy with git. Make a change on my laptop, test it in the different browsers and use the iOS Simulator to take a look at iPad and iPhone browsers. Who knows what someone might use to look at that page when I start using it to market myself. So I make some tweaks, some small, some bigger &#8211; I had to script a few changes for the iPhone because the screen is so small. I commit a series of changes and push a changeset. Then, and this is what I think is great &#8211; I ssh into my bluehost account and change to the online resume directory and all I have to do is git pull. There is no ftp all the files over to the webserver, there is no scp a tarball, delete the old files and unpack the new ones. It is just update the live version and go on about my day.

The importance of tools in helping me is no different than the ones my dad has that he used to build, fix and modify the home I grew up in. The parallells between the real world and the digital world amaze me and the skills I saw Dad use to troubleshoot still apply, even though the tools in play are completely different.