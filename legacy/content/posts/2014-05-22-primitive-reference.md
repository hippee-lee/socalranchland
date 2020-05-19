---
id: 5907
title: Primitive Reference
date: 2014-05-22T17:14:25+00:00
author: matth
layout: post
guid: http://hippeelee.com/?p=5907
permalink: /2014/05/22/primitive-reference/
categories:
  - Computing
---
I routinely take the JavaScript primitives for granted. Sure, when I sit there and think about it I can come up with most of them and describe their properties. In more detail and for faster reference in the future, here are the JavaScript Primitives as I know them. More details and fun facts can be found at the [Global Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects) page of the mozilla developer documentation site.<!--more-->

<div>
  <div class="sectionblock">
    <ul>
      <li>
        <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String">String</a> &#8211; The <strong>String</strong> object is a constructor for strings, or a sequence of characters: var test = &#8220;a new string&#8217;. If you want all the characters available to you you could use the constructor: var test = new String(&#8216;a new string&#8217;)
      </li>
      <li>
        <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number">Number</a> &#8211; The <strong>Number</strong> object is a wrapper object allowing one to work with numerical values. A number object is created with the Number() constructor: var test = new Number(11) or var test = 11
      </li>
      <li>
        <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean">Boolean</a> &#8211; The <strong>Boolean</strong> object is a wrapper for a boolean value. var test = true. I haven&#8217;t used it but you can instantiate them with a Constructor function to get the Boolean object and its methods.
      </li>
      <li>
        <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object">Object</a> &#8211; The <strong>Object</strong> Constructor creates an object wrapper. I have never used the constructor mentor, I just shortcut it with var test = {}
      </li>
      <li>
        <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">Array</a> &#8211; The <strong>Array</strong> primitive is a type for arrays, a high level list like object
      </li>
      <li>
        <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/NaN">NAN</a> &#8211; The <b>NAN</b> is a global property ( much less yummy than it&#8217;s distant cousin naan) that is a value representing Not-A-Number
      </li>
      <li>
        <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined">Undefined</a> &#8211; <strong>undefined</strong> is a global property representing the value undefined
      </li>
      <li>
        <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp">RegExp</a> &#8211; The <strong>RegExp </strong>is an object that can be used for matching patterns in text. I have used both literal and Constructor patterns to instantiate them but prefer the literal method for succinctness.
      </li>
    </ul>
    
    <p>
      In the really real world, there are quite a few more &#8216;Primitive&#8217; types in JavaScript. But these are my best friends in daily work when it targeted at the web browser.
    </p>
  </div>
</div>