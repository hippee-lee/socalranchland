---
id: 6301
title: Yosemite Bluettooth Connectivity Fix
date: 2015-05-15T15:41:56+00:00
author: matth
layout: post
guid: http://hippeelee.com/?p=6301
permalink: /2015/05/15/yosemite-bluettooth-connectivity-fix/
categories:
  - AtWork
  - Computing
  - Hack
---
I have been having issues with my trackpad and bluetooth keyboard reconnecting to after I wake up from a sleep session. Only twice now but the same thing. Instead of restarting (which will fix it) you can drop into the command line and run these two commands:

  1. > sudo kextunload -b com.apple.iokit.BroadcomBluetoothHostControllerUSBTransport

  2. > sudo kextload -b com.apple.iokit.BroadcomBluetoothHostControllerUSBTransport