---
id: 6370
title: Modifying Phone Links For Screens
date: 2015-12-15T19:41:06+00:00
author: matth
layout: post
guid: http://hippeelee.com/?p=6370
permalink: /2015/12/15/modifying-phone-links-for-screens/
categories:
  - Computing
  - HTML/CSS
  - UI/UX
---
### Your Problem

So you have a link thats a phone number. You have this because you want the link to auto dial when on a phone but look like text and not have any functionality when on a screen larger than a phone. As an engineer you don&#8217;t want to duplicate html to provide this feature and would love if css had a way to encapsulate this on one place. What can we do?

Try something like this:

<pre class="EnlighterJSRAW" data-enlighter-language="css" data-enlighter-theme="minimal">a {
  @include rem(font-size, 16px);

  @include media('&lt;tablet') {
    @include rem(font-size, 12px);
  }

  @include media("&gt;=tablet") {
    &[href^="tel"]{
      cursor: default;
      pointer-events: none;
    }
  }

  @include media("&lt;tablet") {
    &[href^="tel"]{
      text-decoration: underline!important;
    }
  }
}</pre>

<pre class="EnlighterJSRAW" data-enlighter-language="html" data-enlighter-theme="minimal">&lt;a href="tel:800-123-4567"&gt;(800) 123-4567&lt;/a&gt;</pre>

### Notes

This is sass and I am using sass-rem for typography and include-media for media queries.