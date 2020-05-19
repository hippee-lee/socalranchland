---
id: 997
title: Practical awk/sed For My Job
date: 2009-04-20T09:49:05+00:00
author: matth
layout: post
guid: http://propri.us/wp/?p=997
permalink: /2009/04/20/practical-awksed-for-my-job/
aktt_tweeted:
  - "1"
  - "1"
  - "1"
categories:
  - Computing
---
Client gave me a list of do not call numbers that has 10 digits on a line. We only have 3, 6 and 7 digits phone scrubs. Using the 7 digit scrub I should be able to use the file the client gave us as a seven digit scrub if I just remove the last three digits from each number in the clients do not call list. The clients list has 686,930 numbers in it.

My usual approach of recording an emacs macro just bogged down the computer and there is also this weird error when I use C-u with large numbers (i gave it the prefix of 100k) and it bombed out after 25k or so).

Anyway, I though about it for a minute and then played around with awk and sed until I came up with this:

> awk &#8216; {print $1} &#8216; UT\_suppress.txt | sed &#8216;s/\[0-9\]\[0-9\][0-9]$//&#8217; > UT\_supress_7digit.txt

Done in less than a minute and I now have a file with seven digits on each line that will not send any numbers on the clients do not call list. <span style="text-decoration: line-through;">Now I am just waiting for the utility script to load that file into the database and its not nearly as fast as awk<!--more--> and sed. So, I have time to write this 🙂</span>

Yeah, so that script just locked up my browser. A slightly modified file via:

> cat UT\_suppress\_7.txt | uniq > UT\_suppress\_7_uniq.txt

only has 189k lines in it. Maybe the upload script will like that better.