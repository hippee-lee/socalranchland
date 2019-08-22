---
id: 5853
title: Provider vs. Service vs. Factory
date: 2014-05-05T02:06:37+00:00
author: matth
layout: post
guid: http://hippeelee.com/?p=5853
permalink: /2014/05/05/provider-vs-service-vs-factory/
categories:
  - (intro)Spection
---
I return to the following three links when I need to refresh my memory or explain to someone else the differences. They have served me well as the first one is participated in by Miško Hevery. The first link is gold where Miško answers and expands a bit.

  1. [Angular Mailing List](https://groups.google.com/forum/#!msg/angular/56sdORWEoqg/HuZsOsMvKv4J )
  2. [Xebia Blog Post](http://blog.xebia.com/2013/09/01/differences-between-providers-in-angularjs/)
  3. [StackOverflow Answers](http://stackoverflow.com/questions/15666048/angular-js-service-vs-provider-vs-factory/20613879#20613879)
  4. [Angular Documentation](https://docs.angularjs.org/guide/providers) (much improved as of May 2014)

<!--more-->

There is one more SO link that has an even better answer than the on provided but I&#8217;ll have to ask my co-worker on monday for it. It&#8217;s better because it answers the &#8216;why&#8217; one is different and this shows how without code examples which always confuse me. Then it sums up with a very simple chart at the bottom. I would look for it right now but my H is is asking why it takes so long to leave a note 🙂 Hacker News is not letting one leave comments right now so I&#8217;m putting this here since I want to expand on it with the link from Tsanko next week.

Ok, she just said &#8220;c&#8217;mon daddy its your turn.&#8217; rolled her eyes and followed up with &#8220;Shouldn&#8217;t you be here? It&#8217;s your turn.&#8221; Turns out I lost the scrabble game anyway &#8211; 16 triangles to 10 because in this version one gets a triangle for completing preset words on the board in order of letters.

Weird, so Monday when I talked to T, we looked at SO together and he was just as confused as I was. The original answer we both liked for its clarity was gone. While the existing answers are good they are all similar to the &#8220;explanation with an example.&#8221; I much prefer an explanation with here is how fundamentally they differ and why that matters without code. Oh well, the link to the angular mailing list is a welcome addition. It would be nice if the original form of the answer that clicked with my mind had been preserved.

Fair enough H. I&#8217;ll come back to this later

&#8230; As the night nights pass and children sleep, I come back to this though in the morning and roughly I remember the table data points as thus (also stealing a bit from the first link above so I can just come here):

#### Services

  * Are Singletons
  * Invocation: returns new instances of its functions (ie invoking myService.myFn() returns a new instance of the function in MyService)
  * Cannot be configured during angular config phase

#### Factories

  * Are Singletons
  * Invocation of myFactory.myFn() returns a value from the Fn referenced
  * Cannot be configured during angular config phase

#### Providers

  * Are Singletons
  * Invocation: returns? &#8216;you are provided with a new ProviderFn().$get() -> constructor fn is instantiated before $get() is called
  * Can be configured during the modules config phase.

I did find a useful table taken from #4 from the list at the top of this post:

[<img class="aligncenter wp-image-5897 size-full" src="http://localhost/wp-content/uploads/2014/05/Screen-Shot-2014-05-19-at-10.40.23-AM.png" alt="Screen Shot 2014-05-19 at 10.40.23 AM" width="901" height="200" srcset="http://localhost/wp-content/uploads/2014/05/Screen-Shot-2014-05-19-at-10.40.23-AM.png 901w, http://localhost/wp-content/uploads/2014/05/Screen-Shot-2014-05-19-at-10.40.23-AM-300x67.png 300w, http://localhost/wp-content/uploads/2014/05/Screen-Shot-2014-05-19-at-10.40.23-AM-768x170.png 768w" sizes="(max-width: 767px) 89vw, (max-width: 1000px) 54vw, (max-width: 1071px) 543px, 580px" />](http://localhost/wp-content/uploads/2014/05/Screen-Shot-2014-05-19-at-10.40.23-AM.png)

&nbsp;