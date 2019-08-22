---
id: 1034
title: Unbracket Anything
date: 2009-04-29T21:31:05+00:00
author: matth
layout: post
guid: http://propri.us/wp/?p=1034
permalink: /2009/04/29/unbracket-anything/
aktt_tweeted:
  - "1"
  - "1"
  - "1"
categories:
  - Computing
  - HTML/CSS
---
Interesting, you can remove everyhing between bracktes (<>). It works with html and I think it handle xml but didn&#8217;t test that for my homework. 

sed &#8216;s/< [^>]*//g&#8217;

It finds the first < character and then deletes all text up to and including the next > character. Interesting. 

You could rehtml stuff but it might take several different scripts. There may be better ways to rehtml stuff.