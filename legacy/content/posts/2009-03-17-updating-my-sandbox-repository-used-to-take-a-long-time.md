---
id: 844
title: Updating My Sandbox Repository Used To Take A Long Time
date: 2009-03-17T08:49:00+00:00
author: matth
layout: post
guid: http://propri.us/wp/?p=844
permalink: /2009/03/17/updating-my-sandbox-repository-used-to-take-a-long-time/
aktt_tweeted:
  - "1"
  - "1"
  - "1"
categories:
  - Computing
---
I have been spending more time in my sandbox at work lately and each time I need to go into the seperate parts of the system to update my sandbox form the repository trunk. Now that I have set up my ssh keys and no longer need to type in a pwd twenty times there was no reason to have to run svn update blah for the four parts of our system that I look at or use.

Enter update\_svn.sh and I can just ssh into the server,Ã‚Â cd to my sandbox and run update\_svn.sh and voila I get this

> $ ./update_svn.sh
  
> updating blah
  
> &#8212;&#8212;&#8212;&#8212;&#8212;
  
> Fetching external item into &#8216;blah/blah&#8217; Fetching external item into &#8216;blah/lib/ajax&#8217; External at revision 5734. Fetching external item into &#8216;blah/lib/sarissa&#8217; External at revision 5734. At revision 5734. Fetching external item into blah/blah/lib/custom&#8217; External at revision 5734. At revision 5734.
  
> &#8212;&#8212;&#8212;&#8212;&#8212;
  
> blah updated
  
> &#8212;&#8212;&#8212;&#8212;&#8212;
  
> updating foo
  
> &#8212;&#8212;&#8212;&#8212;&#8212;
  
> U foo/bin/foo.pl Updated to revision 5734.
  
> &#8212;&#8212;&#8212;&#8212;&#8212;
  
> foo updated
  
> &#8212;&#8212;&#8212;&#8212;&#8212;
  
> updating bar
  
> &#8212;&#8212;&#8212;&#8212;&#8212;
  
> Fetching external item into &#8216;bar/lib/ajax&#8217; External at revision 5734. Fetching external item into &#8216;bar/lib/sarissa&#8217; External at revision 5734. At revision 5734.
  
> &#8212;&#8212;&#8212;&#8212;&#8212;
  
> bar updated
  
> &#8212;&#8212;&#8212;&#8212;&#8212;
  
> updating baz
  
> &#8212;&#8212;&#8212;&#8212;&#8212;
  
> At revision 5734.
  
> &#8212;&#8212;&#8212;&#8212;&#8212;
  
> baz updated
  
> &#8212;&#8212;&#8212;&#8212;&#8212;
  
> sandbox repositiory updated

Of couse the names and paths are changed for obvious reasons. But it sure makes it convienient to svn update now.Ã‚Â If I really wanted to<!--more--> track how often I was doing it I caould also redirect output to a log file and append a date time stamp at the end where it says sandbox repository updated: YYYY/MM/DD HH:MM.