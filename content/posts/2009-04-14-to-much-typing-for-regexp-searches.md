---
id: 969
title: To Much Typing For Regexp Searches
date: 2009-04-14T11:30:49+00:00
author: matth
layout: post
guid: http://propri.us/wp/?p=969
permalink: /2009/04/14/to-much-typing-for-regexp-searches/
aktt_tweeted:
  - "1"
  - "1"
  - "1"
categories:
  - Computing
  - Emacs
---
I have been getting better at using the regexp search functions in emacs. Today I got tired of all this typing: M-x search-forward-regexp so I bound it to this in my init file:

> (global-set-key (kbd &#8220;C-c sfr&#8221;) &#8216;search-forward-regexp)

Of couse I also bound the opposite:

> (global-set-key (kbd &#8220;C-c sbr&#8221;) &#8216;search-backward-regexp)

I know, I know, how did I get anything done when I had to type out all thise characters before.