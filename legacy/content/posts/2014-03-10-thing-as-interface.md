---
id: 5749
title: Thing As Interface
date: 2014-03-10T14:07:56+00:00
author: matth
layout: post
guid: http://hippeelee.com/?p=5749
permalink: /2014/03/10/thing-as-interface/
categories:
  - Computing
  - UI/UX
  - Visual Thought
---
I have been thinking about why I don&#8217;t want my apps to make me think. I&#8217;m there to do a job and move on. If I have to change this, fix that or connect to the network because the app forgot that it just got the data for this screen a minute ago before I switched apps to check my calendar; then the app is making me do more mental work than I budgeted for the task.<!--more-->

Ok, so whats the $64,000 answer to complicated processes that are not simple point and click interfaces? On the web part of the answer seems to be the marriage of data to the DOM. As SPA frameworks and other web app friends become more powerful the elements that are used as interface no longer contain the data, they have the data and functionality built right in. How Lisp like! And, yay JavaScript.

Thinking about a generic problem thats important to me as it keeps coming back to bother J at work is the folks who stare at spreadsheets all day and want to be able to play with forecasting. They sort of know where they are now based on some numbers, they know what they think other variable and dependent numbers will cost down the road. But how can they compile their numbers, chart out the projections and then play with the variables? I searched but didn&#8217;t see anything in Excel that a non programmer could quickly and easily jump into.

So what is the generic solution to the problem? Here is the problem statement:

  * I have several columns of data
  * Some columns are dependent on other columns
  * I want to &#8216;see&#8217; the data world as it is today
  * I want to play with ranges of data to change tomorrows data world and I want to do this from a visual standpoint ( ala the worrydream.com genius ) and with intuitive interaction

With modern tools the data can become the interface but this makes it more advanced, more complicated and I don&#8217;t want that. Need to think more on this problem and mock up a prototype to understand the connections.