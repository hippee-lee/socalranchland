---
id: 354
title: slime(y) confusion
date: 2008-10-08T11:43:00+00:00
author: matth
layout: post
guid: http://propri.us/wp/?p=354
permalink: /2008/10/08/slimey-confusion/
categories:
  - Emacs
---
I was trying to run slime today to play with something and I kept getting this error:

> debugger invoked on a SB-INT:SIMPLE-FILE-ERROR:
> 
> Ã‚Â Ã‚Â Couldn&#8217;t load
> 
> Ã‚Â Ã‚Â #P&#8221;/Users/matthew/.slime/fasl/2008-07-06/sbcl-1.0.21-darwin-x86/swank-sbcl.fasl&#8221;:
> 
> Ã‚Â Ã‚Â file does not exist.
> 
> Type HELP for debugger help, or (SB-EXT:QUIT) to exit from SBCL.
> 
> restarts (invokable by number or by possibly-abbreviated name):
> 
> Ã‚Â Ã‚Â 0: [ABORT] Exit debugger, returning to top level.
> 
> (LOAD
> 
> Ã‚Â #P&#8221;/Users/matthew/.slime/fasl/2008-07-06/sbcl-1.0.21-darwin-x86/swank-sbcl.fasl&#8221;)[:EXTERNAL]

After googling and trying different things I found the problem. Turns out, I had two (require &#8216;slime) &#8216;s in my .emacs file. d&#8217;oh. I am not sure why that caused the problem though but things are working now and I have upgraded to sbcl version 1.0.21.