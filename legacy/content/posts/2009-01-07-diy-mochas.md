---
id: 569
title: DIY Mochas
date: 2009-01-07T10:21:57+00:00
author: matth
layout: post
guid: http://propri.us/wp/?p=569
permalink: /2009/01/07/diy-mochas/
aktt_tweeted:
  - "1"
  - "1"
  - "1"
categories:
  - php
---
Make a home-made Mocha:
  
1) brew some yummy costa rican coffee
  
2) in coffee cup add some coffee mate + two spoonfulls of cocoa
  
3) pour in an equal amount of hot coffee
  
4) stir until cocoa substrate is all in solution
  
5) fill cup with the rest of your coffee
  
6) enjoy!

In other news I came across some very useful code for dealing with dates in php:
  
strtotime() is a php function that takes a wide range of text inputs and returns a unix timestamp. For example I needed to take a date in the format of 2009-03-19 and check to see if its in the range of now-11 months and now+8 months. Thank you strtotime():

> //create a date range object (now-11 months to now+8 months) and check to see if users due date is in the acceptible range
  
> $range[&#8216;start&#8217;] = strtotime(&#8220;-11 months&#8221;); //now &#8211; 11 months
  
> $range[&#8216;end&#8217;] = strtotime(&#8220;+8 months&#8221;); //now + 8 months
  
> $range[&#8216;due_date&#8217;] = strtotime($yyyy . &#8216;/&#8217; . $mm . &#8216;/&#8217; . $dd);
> 
> if( ($range[&#8216;start&#8217;] < $range['due\_date']) && ($range['due\_date'] < $range['end']) ) { debug("due date is within the range"); return true; } else { $_REQUEST['q21845'] = "Due Date Note Valid"; debug("due date is not within the range"); return true; }</blockquote>