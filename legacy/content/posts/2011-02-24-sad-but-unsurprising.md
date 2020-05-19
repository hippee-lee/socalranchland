---
id: 1717
title: Sad But Unsurprising
date: 2011-02-24T10:33:50+00:00
author: matth
layout: post
guid: http://hippeelee.com/blog/?p=1717
permalink: /2011/02/24/sad-but-unsurprising/
categories:
  - JavaScript
---
The following JavaScript doesn&#8217;t work in IE:

> var list = [&#8216;.item1&#8217;, &#8216;.item2&#8217;, &#8216;.item3&#8217;, &#8216;&#8230;
> 
> list.forEach(
> 
> function (item) {
> 
> $(item).hide();
> 
> });

Sad. I wonder if the array object could be extended r prototyped to add that if IE is detected?