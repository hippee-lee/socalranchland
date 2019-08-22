---
id: 5539
title: Bundle Bit Removal
date: 2013-11-24T17:25:29+00:00
author: matth
layout: post
guid: http://hippeelee.com/?p=5539
permalink: /2013/11/24/bundle-bit-removal/
categories:
  - AtHome
  - Computing
---
Used when I copied my laptop photo library into a media archive and Finder saw the parent directory as a package instead of a folder.

> <pre><span style="color: #003366;">xattr -d com.apple.FinderInfo ~/Desktop</span></pre>