---
id: 1699
title: 'Because It&#8217;s There'
date: 2011-02-18T18:36:38+00:00
author: matth
layout: post
guid: http://hippeelee.com/blog/?p=1699
permalink: /2011/02/18/because-its-there/
categories:
  - Computing
  - JavaScript
  - Matt
---
I read a post by someone who used to work at youtube a while back. He was talking about how most of the people he interviewed could not work on the DOM with-out jQuery.

I like jQuery, it makes my job much, much easier even in the bastardized form I have to use it in. But, I liked the challenge and decided to work on the DOM with out a library, only using pure JavaScript.

It took me a few weeks of 2 hour nightly sessions to prototype, but I have something that runs. You can see the repository <a href="https://bitbucket.org/hippeelee/ticker" target="_blank">here</a>, and I added a page called [ticker](http://hippeelee.com/ticker.html). Its a bare bones demo and still more concept than practical utility, but I am having fun fleshing it out.

I know there are more elegant tools and plug-ins that do the same thing. It feels good to do it for myself, just because I can. A bit like cultivating a home garden. Sure, I am not on the scale as the professionals and sure, my solution is not ideal. But that wasn&#8217;t the point &#8230;

The DOM with images was there and now I can make them do what I want. I learned a<!--more--> bit more about JavaScript along the way and thats always fun too. I also learned that mogrify is a similar to sips on OSX. The images I uploaded were full size and were taking forever to fully load. It was kind of funny to watch partially loaded images cycle around until they were all loaded into the DOM. Anyhow, if you are on linux and need to (quickly) resize a batch of images you can man mogrify or: $ mogrify -resize 800 /path/to/img/*.JPG. I think it is part of imagemagick

 <strong style="font-style: italic;"></strong>but I am not to familiar with that library.