---
id: 1146
title: dotemacs debug
date: 2009-05-29T09:03:17+00:00
author: matth
layout: post
guid: http://propri.us/wp/?p=1146
permalink: /2009/05/29/dotemacs-debug/
aktt_tweeted:
  - "1"
  - "1"
  - "1"
categories:
  - Computing
  - Emacs
---
I have been getting some strange errors on startup since I put my home directory under mercurial and have been trying to keep OSX Tiger(PPC) in sync with Leopard(Intel). Anyhow I was working through the errors on the Leopard box and got tired of quiting/restarting emacs. looking at an <a title="emacs eval" href="http://hippeelee.com/blog/?p=871" target="_self">older post</a> and doing a quick C-h k C-x C-e showed me that its an eval function. I have icicles installed so when I M-x eval TAB I got a list of all the eval commands available and there is the command of today:

> M-x eval-buffer

My debugging went faster after that and I learned something new.