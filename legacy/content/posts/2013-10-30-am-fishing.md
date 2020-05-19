---
id: 5524
title: AM Fishing
date: 2013-10-30T15:49:01+00:00
author: matth
layout: post
guid: http://hippeelee.com/?p=5524
permalink: /2013/10/30/am-fishing/
categories:
  - Uncategorized
---
I had a minor issue this morning with my work computer. It&#8217;s set up with OSX Mavericks and I use two external monitors. The most anticipated feature I was looking for was the real support for full screen modes on multiple monitors and I have been making heavy use of it. Since I work in a PCI compliant environment I have a five minute time out that locks the system and also requires a password when waking up. yesterday and today I had an issue.

My mouse moves by no left clicks are registered on the system. Weird. Ok, yesterday I just did a hard reset. Today I really didn&#8217;t want to do that, to many servers to restart and files open for the AngularJS app I am working on to remember and reopen.

Five minutes searching the internets led me to this:

> |ruby-1.9.3-p327| matth-mbp in ~/Dev/sites/site-ux
> 
> ± |master ✗| → killall -KILL SystemUIServer

The important thing is killall -KILL SystemUIServer

I am guessing here but SystemUIServer is an object that supports UI Interaction and killing it causes it to bounce. ISK, it fixed my problem and I am glad I can fish for myself rather than doing a full restart every time. Ok, back to the AngularJS issue of how to pass the results of a promise through to a linked directive. Hmmm. Not much on the internets for this one.