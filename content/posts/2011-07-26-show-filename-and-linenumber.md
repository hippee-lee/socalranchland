---
id: 2469
title: Show filename and linenumber
date: 2011-07-26T16:25:59+00:00
author: matth
layout: post
guid: http://hippeelee.com/blog/?p=2469
permalink: /2011/07/26/show-filename-and-linenumber/
categories:
  - Computing
tags:
  - Bash
  - find
  - grep
---
When searching for files in a bash shell, show the file and line that was matched:
  
find . -name *.js -print0 | xargs -0 grep -n -H set\_up\_uploadify

This could be rolled into a custom script with file type and arg1 and pattern as arg2.