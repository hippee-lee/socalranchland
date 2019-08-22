---
id: 5405
title: Advice For Getting Started With GIT And Angular
date: 2013-09-07T22:45:48+00:00
author: matth
layout: post
guid: http://hippeelee.com/?p=5405
permalink: /2013/09/07/advice-for-getting-started-with-git-and-angular/
categories:
  - Uncategorized
---
First, clone an existing project, don&#8217;t inherit a project from github thats actively developed by someone smarter than you instead of an overseas contractor who was also learning Angular for the first time 😉<!--more-->

Several times different folks on my team have said I should do some demos on the toolchain (git + nom/bower/grunt + Angular). I just don&#8217;t have the time to put anything together right now, and, I am still a novice when it coms to anything more than trying to get things done. So I am writing my thoughts down for the future when time is endless and energy is abundant.

I find that I learn best when I jump right in and collect a list of questions that I can file away for later once I have some experience using the tool(s). I would suggest the same if you are approaching a modern web client for the first time. Related, I was asked on Friday how I would approach things related to version control and Github. Keep in mind that what works for me is closely related to idiosyncrasies and personal preferences.

Here are the GIT work flow guidelines (Think Jack Sparrow) that work for me &#8211; ymmv, especially since most of the code outside of the web client I work on is in subversion and for that, I use git as my svn client:

  * Clone the repo from Github
  * Keep master up to date by pulling often (at least thrice daily)
  * Branch for each ZUM Issue and rebase or merge (I don&#8217;t have a feel for one or the other yet) master onto the development often (at least thrice daily)
  * When a branch with your ZUM issue is addressed or fixed: $ git rebase master then, git checkout master then, git merge your-sum-branch. Finally git push (to the master on github)
  * I push my local branches to github pretty often but thats just me wanting a backup of the repp&#8217;s, I delete them when I am finished with them.
  * It is entirely possibleI only know enough of GIT to shoot myself in the foot so you should take all of the above with a grain of salt; internet search and StackOverflow are your friends but be suspicious of even them

SInce I was thinking about it, here are some thoughts based on my introduction to Angular: ymmv

  * Pick an issue, story, or area and create an exploratory branch off master
  * Run it with grunt server, forget setting up/hooking into apache it&#8217;s not needs to learn development
  * Commit often (I prefer the command line for this over the gui&#8217;s &#8211; its faster. I do use the Atlassian SourcecTree tool for pushing my local branches and fetching as well as getting a visual look at how things fit together)
  * Commit often when you make a change and its still running. Leave yourself a note.
  * Muck around with all three (scss, JavaScript and html) levels till you break it and can&#8217;t fix it, then do a $ git reset &#8211;hard (This wipes out all uncommitted changes and restores you back to you last hopefully recent and working commit)
  * Since we are all Angular beginners (at my company we only ramped up Angular development in May and I didn&#8217;t jump in over my head until late June), if you fix something or make a change you think should go into master, <del>grab me and I can help</del> ask someone to help you merge it into master or do a pull request <del>and I</del> that someone more knowledgeable can review it/m,edge it asynchronously
  * If you are doing anything css related push the dist/ filles to an apache server (I have a simple grunt\_and\_deploy script that does this for me) and test in IE9/10 first (if you have to support them)
  * $ grunt is your friend, even when it yells at you. It will jslint the code base for us. (I try not to commit to master unless grunt is happy but it&#8217;s not happy right now and there are some other things to attend to at the moment
  * $ grunt server is also your (development) friend along with a decent JS/CSS/HTML editor that lets you debug in the browser. I find myself jumping back and forth between Chromes built in tools and the tools for my editor
  * It is entirely possible that I only know enough JavaScript + Angular to shoot myself in the foot so you should take the above with a grain of salt; internet search and StackOverflow are your friends but be suspicious of even them