---
id: 873
title: Matthews Fizzbuzz
date: 2009-03-24T13:56:51+00:00
author: matth
layout: post
guid: http://propri.us/wp/?p=873
permalink: /2009/03/24/matthews-fizzbuzz/
aktt_tweeted:
  - "1"
  - "1"
  - "1"
categories:
  - Computing
  - Emacs
  - JavaScript
---
During lunch I came across a reference to the fizzbuzz question (ie for the integers between 1-100 &#8230; print fizz if the number is divisble by 3, buzz if divisible by 5 and fizzbuzz if divisible by both) in reading someone&#8217;s blog. I have always said to myself, I need to see how long it will take me to solve that.

**Javascript:**

> var fizzbuzz = function(){
> 
> document.writeln(&#8220;Matthews Fizzbuzz&#8221;);
> 
> document.writeln(&#8220;<br />&#8221;);
> 
> //an array to hold my numbers and numses
> 
> var nums = new Array();
> 
> for (x = 1; x < 101; ++x){
> 
> nums.push(x);
> 
> }
> 
> for (z=0; z < nums.length; ++z){
> 
> if(nums[z] % 3 == 0 && nums[z] % 5 == 0){
> 
> document.writeln(&#8220;fizzbuzz&#8221; + &#8220;<br />&#8221;);
> 
> }else if(nums[z] % 3 == 0){
> 
> document.writeln(&#8220;fizz&#8221; + &#8220;<br />&#8221;);
> 
> }else if(nums[z] % 5 == 0){
> 
> document.writeln(&#8220;buzz&#8221; + &#8220;<br />&#8221;);
> 
> }
> 
> else{
> 
> document.writeln(nums[z] + &#8220;<br />&#8221;);
> 
> }
> 
> }
> 
> }
> 
> var start = new Date();
> 
> start = start.getTime(); Ã‚Â // returns millisecs since epoch which is what I want since this operation takes less than a second
> 
> start += parseInt( start );
> 
> fizzbuzz();
> 
> var end = new Date();
> 
> end = end.getTime();
> 
> end += parseInt( end );
> 
> document.writeln(&#8220;This took &#8221; + (end &#8211; start) + &#8221; milliseconds to run&#8221;);

Notes: it took me about five minutes give or take and I have seen it report between 2-4 milliseconds to run. The current program is 33 lines of code.

**Emacs Lisp:**

> ;;print out<!--more--> a list of numbers, one per line, 1 &#8211; 100, if divisible by 3 print fizz, if divisble by 5 print buzz if divisible by both print fizzbuzz
> 
> ;;time how long it takes to run fizzbuzz
  
> (defvar \*emacs-fb-start\* (current-time))
> 
> (setq nums 1)
> 
> (while (< nums 101)
  
> (if (and (= 0 (% nums 3)) (= 0 (% nums 5)))
  
> (print &#8220;fizzbuzz&#8221;)
  
> (if (= 0 (% nums 3))
  
> (print &#8220;fizz&#8221;)
  
> (if (= 0 (% nums 5))
  
> (print &#8220;buzz&#8221;)
  
> (print nums))))
  
> (setq nums (+ nums 1)))
> 
> ;;this must be last line to calculate fizzbuzz runtime
  
> (message &#8220;Fizzbuzz ran in %dms&#8221; (destructuring-bind (hi lo ms)
  
> (current-time) (- (+ hi lo) (+ (first \*emacs-load-start\*) (second
  
> \*emacs-fb-start\*)))))

Notes: this took me a bit longer since I am used to stealing my emacs lisp code from google. I had to go in and read the emacs-lisp-intro info doc included with emacs to figure out how to run the while if and multiple conditionals for the divisible by five and 3 check. I still need to put a timer on it but I can steal that code (stolen from someone elses .emacs file) from my .emacs file which times emacs when I start it up. I borrowed the timer code from .emacs and i think its output is wrong: Fizzbuzz ran in 186ms. The current program is 21 lines of code with blank lines and comments, cool!

**bash**

> #!/bin/bash
> 
> before=&#8221;$(date -j -f &#8220;%a %b %d %T %Z %Y&#8221; &#8220;\`date\`&#8221; &#8220;+%s&#8221;)&#8221;
> 
> echo &#8220;=========================Starting Fizzbuzz: $before=========================&#8221;
  
> num=1
  
> while [ $num -lt 101 ]; do
  
> #if % 3&&5 print fizzbuzz
  
> if [ $(( $num % 5 )) -eq 0 ] && [ $(( $num % 3 )) -eq 0 ] ; then
  
> echo &#8220;fizzbuzz&#8221;
  
> elif [ $(( $num % 5 )) -eq 0 ] ; then
  
> echo &#8220;buzz&#8221;
  
> elif [ $(( $num %3 )) -eq 0 ] ; then
  
> echo fizz
  
> else
  
> echo $num
  
> fi
  
> let num=num+1
  
> done
  
> after=&#8221;$(date -j -f &#8220;%a %b %d %T %Z %Y&#8221; &#8220;\`date\`&#8221; &#8220;+%s&#8221;)&#8221;
> 
> elapsed=&#8221;$(expr $after &#8211; $before)&#8221;
  
> echo &#8220;Time elapsed: $elapsed&#8221;
> 
> echo &#8220;=========================End Fizzbuzz: $after=========================&#8221;
  
> exit 0

Notes: This was pretty straight forward as I could use the javascript logic flow and just substitute the bash syntax. The time does&#8217;t work very well since it only resolves to seconds and I think this goes faster than that. I would need to find a way to get microseconds and I didn&#8217;t see anything like that in the data man page. Lines of code: 26 total, no comments.