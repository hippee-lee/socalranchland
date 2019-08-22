---
id: 4546
title: The New Slideshow
date: 2012-03-08T21:03:29+00:00
author: matth
excerpt: I have come across several neat JavaScript programs that take advantage of all the CSS3 fun you can do in modern browsers. Each time I see a new one idas go racing through my head. I can do this or that or ....
layout: post
guid: http://hippeelee.com/blog/?p=4546
permalink: /2012/03/08/the-new-slideshow/
categories:
  - (intro)Spection
  - Computing
  - UI/UX
tags:
  - JavaScript
  - Self
---
I have come across several neat JavaScript programs that take advantage of all the CSS3 fun you can do in modern browsers. Each time I see a new one idas go racing through my head. I can do this or that or &#8230;.

A couple weeks ago I got one of those mailer brochures from a credit card company with pretty images and pithy tag lines telling me all about their product. I don&#8217;t need any more credit cards right now. But it did get me thinking, how could I do this on a webpage? So I marked it up with one of Hannah&#8217;s pens into some simple markup for the different pieces on each page and put it on my desk. Then I cleaned the office and tossed it. However, the idea continued to roll around in my head and about a week later I finished reading [The Start Up Of You](http://www.thestartupofyou.com/). I joined the group on LinkedIn. Why not, I have been spending quite a bit of time on there looking for reasonable jobs lately. So it was easy to join and nice to come across variations of ideas in the book as well as intelligent discussion about how to<!--more--> apply them.

Then, last week I got involved in a discussion thread about the benefits of soft assets online. Things like a personal and professional blog or a portfolio. Should you have one, should you keep personal and professional separate online? Things like that &#8211; it was an interesting discussion that kept waking me up at 5:30am. It brought up this question in my mind: Why not create a digital brochure with one of the cool JavaScript tools out there as a self promotional piece. I finally sat down and put something together with [Reveal.js](https://github.com/hakimel/reveal.js). I think it was the combination of the digital brochure idea coupled with the advice to learn how to better promote myself and a desire to create something that I thought was cool. The idea is not a resume, not a cover letter. Those things need to be specifically crafted for an employer and I rarely use the general core version that is <a href="http://hire.hippeelee.com" target="_blank">here</a> as it is. Plus, I don&#8217;t think resumes and cover letters are very cool and these days, the importance of them is a little suspect with all the buzz word filters out there.

The idea is to create my own marketing collateral as part of a larger campaign. Get what I saw inside my head, a merger of some of the favorite photographs I have taken over the past few years with a tag line or phrase that reflects my personality, and make it into a digital brochure of sorts. After getting a bit of feedback that helped guide the removal of things not needed, I ended up with 7 slides, one even has an attempt at a haiku poem. I modified Reveal just a bit. I needed to slow down the transitions and I also wanted to make my slides full screen. Thats how I saw it in my head. After gauging a reaction and some feedback I am not sure if that works or not. Digging through the source though it might be possible to add a setting that makes each slide &#8220;full screen&#8221; (not the OSX full screen), just the full size of the window.

Anyway, in parlance with the theme of permanent beta in The Start Up Of You, I put it up on its own site <a href="http://matt.hippeelee.com" target="_blank">here</a>. While not on par with an Apple marketing campaign, I think its a good start to reflecting out some of the things I see inside and I can always continue to iterate on it as I change or get good feedback. There were some good questions fed back to me that I still don&#8217;t have a good answer to. Who is the target audience? I don&#8217;t know yet. Why would I send them a link to that piece and what am I trying to say? Well, that one I do know, sort of. I wanted to communicate technical competence (implementing the slideshow, the keyboard navigation and simple transforms with flexible content) and include an abstract, creative element in the words chosen for each image, where some of the phrases were placed and how they moved when you resize the window. I&#8217;m not sure if it worked but it was good to be making something.

Two things came out of this. Well, three if you [include the actual page](http://matt.hippeelee.com) itself. I liked the challenge of finding images that speak to me and figuring out what they say to me. There has to be something else I can do with this concept &#8211; snowboarding, nature, politics? Hmmm, nature or politics shouldn&#8217;t be too hard. The catch is I have to use my own images for the message. The second thing is that I should modify Reveal so that I don&#8217;t have to do the full window size in the css. Make it just another option to pass in when Reveal is initialized.