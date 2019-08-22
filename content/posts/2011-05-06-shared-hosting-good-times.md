---
id: 2267
title: Shared Hosting, Good Times
date: 2011-05-06T08:53:33+00:00
author: matth
layout: post
guid: http://hippeelee.com/blog/?p=2267
permalink: /2011/05/06/shared-hosting-good-times/
categories:
  - Blog
tags:
  - Media
  - troubleshooting
  - web
---
<figure id="attachment_2268" style="width: 189px" class="wp-caption aligncenter"><a rel="attachment wp-att-2268" href="http://hippeelee.com/blog/2011/05/shared-hosting-good-times/uh-oh/"><img class="size-full wp-image-2268" title="Site Error" src="http://hippeelee.com/blog/wp-content/uploads/2011/05/uh-oh.jpeg" alt="There was an error" width="189" height="56" /></a><figcaption class="wp-caption-text">There was an error </figcaption></figure> 

&nbsp;

Notes to myself. Using the bluehost site backup tools did not go as expected. One minute there were 300+ public posts the next day there were 72. Weird I thought. I am happy that I did a manual dump last month. Here are the steps I took to restore my content:

  1. Export the remaning blog posts with the export function from my wp-admin export page. Lucky for me the sites small and I can just export everything and still get a reasonably sized file.
  2. From my laptop:
  3. scp last-months-database-backup.sql to my bluehost account
  4. Log into bluehost command line and run the following:
  5. mysqldump -u -p dbname wp_users > wp-users.sql
  6. Open the command line mysql client: mysql -u -p dbname
  7. On the mysql command line client: use dbname
  8. On the mysql command line client: source last-months-database-backup.sql
  9. On the mysql command line client: source wp-users.sql (I think there was a confilct when I did step #9
 10. Go back to the website admin import area
 11. Use the wprdpress admin import function select the file created in step #1.
 12. Be happy I can do this for myself 🙂

Happy Friday!

I think its Time to write my own script that I can run from my laptop. Here is what I<!--more--> need it to do:

  * Log into bluehost account
  * Create an archive of the web root folder and sub-directory&#8217;s
  * Dump the database into the archive
  * scp the backup file from bluehost to my laptop
  * Send myself a notification so I can add redundancy by making sure it gets onto the computer backed up with CrashPlan.

Manually this can be acomplished with the following:

  1. mysqldump -u -p database_name > SITENAME-YYYY.MM.DD.sql
  2. mv SITENAME-YYYY.MM.DD.sql /path/to/website/root
  3. tar -zcvf ~/SITENAME-YYYY.MM.DD.tar.gz /path/to/website/root
  4. exit (leave the webhosting server)
  5. On my laptops command line &#8230;
  6. scp username@host:~/SITENAME-YYYY.MM.DD.tar.gz .

After all of that, I end up with a file on my local computer that I can send to the home computer to be backed up with CrashPlan or put it somewhere else that is safe.