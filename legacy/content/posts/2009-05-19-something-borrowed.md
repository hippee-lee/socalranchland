---
id: 1102
title: Something Borrowed
date: 2009-05-19T08:17:39+00:00
author: matth
layout: post
guid: http://propri.us/wp/?p=1102
permalink: /2009/05/19/something-borrowed/
aktt_tweeted:
  - "1"
  - "1"
  - "1"
categories:
  - Computing
  - Emacs
---
I am borrowing this from the [emacs wiki](http://www.emacswiki.org/emacs/SwitchingBuffers).

> ;; for swaping buffers between frames when the window is split
  
> (defun transpose-buffers (arg)
  
> &#8220;Transpose the buffers shown in two windows.&#8221;
  
> (interactive &#8220;p&#8221;)
  
> (let ((selector (if (>= arg 0) &#8216;next-window &#8216;previous-window)))
  
> (while (/= arg 0)
  
> (let ((this-win (window-buffer))
  
> (next-win (window-buffer (funcall selector))))
  
> (set-window-buffer (selected-window) next-win)
  
> (set-window-buffer (funcall selector) this-win)
  
> (select-window (funcall selector)))
  
> (setq arg (if (plusp arg) (1- arg) (1+ arg))))))
> 
> (global-set-key (kbd &#8220;C-x 4 t&#8221;) &#8216;transpose-buffers)

I have been meaning to find a solution for this for a while. Emacs Wiki, you guide me well. Repeating to self five times: &#8220;Command four tee&#8221;, &#8220;Command 40&#8221;, &#8220;Command 4 t&#8221;, &#8220;Command four t&#8221;, &#8220;Command 4 tee&#8221;

That should stick for a few hours so I can use it a few times.