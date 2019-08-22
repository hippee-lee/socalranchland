---
id: 871
title: Running With elisp
date: 2009-03-24T07:12:35+00:00
author: matth
layout: post
guid: http://propri.us/wp/?p=871
permalink: /2009/03/24/running-with-elisp/
aktt_tweeted:
  - "1"
  - "1"
  - "1"
categories:
  - Computing
  - Emacs
---
I need to remember the other ways to run my elisp code. It will help to be able to do it inline when I want the resutls put into the documet I am editing, it will also help to be able to run a function from where my point currently is when I am figuring out somthing. To that end here are three ways to run elisp code:

  1. C-j: will spit the result into the \*scratch\* buffer when testing scratch code there
  2. M-C-x: will echo the result into the mini buffer when the point is in the function
  3. C-xC-e: will echo the result into the mini buffer when point is just after the last )

These commands also work for atoms: expressions not in parens such as numbers, strings, characters and symbols.