---
id: 5836
title: expect(a).toBe(c)
date: 2014-04-23T20:34:10+00:00
author: matth
layout: post
guid: http://hippeelee.com/?p=5836
permalink: /2014/04/23/expecta-tobec/
categories:
  - Computing
  - JavaScript
---
I was writing some tests for a singleton I need to create and thought this block was cool:

[js]
  
it(&#8216;should be a Singleton object&#8217;, function () {
  
var a = siteDNA.getInstance();
  
var c = siteDNA.getInstance();
  
expect(a).toBe(c);
  
});
  
[/js]