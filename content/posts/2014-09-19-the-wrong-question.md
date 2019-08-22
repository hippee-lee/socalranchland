---
id: 6060
title: The Wrong Question
date: 2014-09-19T18:15:09+00:00
author: matth
layout: post
guid: http://hippeelee.com/?p=6060
permalink: /2014/09/19/the-wrong-question/
categories:
  - (intro)Spection
---
Asking the wrong question is expensive. It eats up time, creates unintended problems with cascading consequences and exhausts your energy. We are looking at appetizing our themes at work. Our themes are simple angular apps that depend on a toolbox of things related to the api, business logic and the desire to provide some out of the box components that just work. For the uninitiated Angular developer this lets them focus on the style and presentation of the app and spend time where they are more comfortable, with the scss (or css if they nee to).

<!--more-->

#### Red Herrings

My opinions and pre conceptions limit the possible solutions and can keep me trying to solve the wrong problem in the wrong way. When the requirement was presented I was skeptical, because I knew a little bit about this:

> [Note: You should not use the ng-app directive when manually bootstrapping your app.](https://docs.angularjs.org/guide/bootstrap)

That made me assume you cannot inject other apps as dependency&#8217;s into other angular apps. Despite knowing how bower_components are (manually) injected into the app. So I read all the way down to there again and went on my way looking for ideas on how to:

  1. Inject  and config a second angular app into a running angular app; despite the fact that it is very clear that this is not possible
  2. Bootstrap one angular app with the same instance or a reference to dependencies from another so I didn&#8217;t have to worry about intra-app communication and other things related to how we are using the services

Red herrings can help you by leading you on paths you didn&#8217;t know about but they can also harm you by locking yourself into limitations that don&#8217;t really exist.

#### Reflection In Progress

Neither of these things was what I needed to do. And it would have helped to reflect more on what I needed to do rather than how I thought it should be done. How I think things should be done are intimately tied to my opinions and preconceptions. Reflecting critically and often will help the honest person balance the pro&#8217;s and cons that Red Herrings provide while asking the right questions.