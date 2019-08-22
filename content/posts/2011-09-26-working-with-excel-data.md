---
id: 2733
title: Working With Excel Data
date: 2011-09-26T14:10:32+00:00
author: matth
layout: post
guid: http://hippeelee.com/blog/?p=2733
permalink: /2011/09/26/working-with-excel-data/
categories:
  - AtWork
  - Computing
  - Emacs
tags:
  - text
---
Excel is blah to work with. A client gives us data made with it though and they put symbols in the text. After trying to cat out the tsv file I found this solution from within emacs:

`M-x replace-regexp<br />
[[:nonascii:]]  RET RET`

It found and replaced the pesky tm symbols in the text file with nothing. I wonder if the [[:nonascii:]] char class is available on the command line in awk or sed?