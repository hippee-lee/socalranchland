---
id: 6241
title: 1.x Directives
date: 2015-02-20T12:31:44+00:00
author: matth
layout: post
guid: http://hippeelee.com/?p=6241
permalink: /2015/02/20/1-x-directives/
categories:
  - (intro)Spection
---
Notes to self & advice to those working in Angular 1.x Land. If you don&#8217;t want to read <a title="this" href="http://www.jvandemo.com/the-nitty-gritty-of-compile-and-link-functions-inside-angularjs-directives/" target="_blank">this</a>, here are three elevator pitch points to consider when understanding directives:<!--more-->

  1. Use the `compile` function to change the original DOM (template element) before AngularJS creates an instance of it and before a scope is created.
  2. Use the `pre-link` function to implement logic that runs when AngularJS has already compiled the child elements, but before any of the child element&#8217;s `post-link` functions have been called.
  3. Use the `post-link` function to execute logic, knowing that all child elements have been compiled and all `pre-link` and `post-link` functions of child elements have been executed.

I disavow any credit for the three points above. [@<span class="u-linkComplex-target">jvandemo</span>](https://twitter.com/jvandemo){.ProfileHeaderCard-screennameLink.u-linkComplex.js-nav} wrote the clear and excellent piece above. This is just my summary of his summary on the article which you ignored if you are reading this far 🙂 This post is mainly for a reference at my fingertips later on in the future when I need to real it.