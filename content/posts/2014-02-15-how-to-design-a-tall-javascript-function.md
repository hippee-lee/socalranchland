---
id: 5675
title: How To Design A Tall (JavaScript) Function
date: 2014-02-15T19:18:12+00:00
author: matth
layout: post
guid: http://hippeelee.com/?p=5675
permalink: /2014/02/15/how-to-design-a-tall-javascript-function/
geo_latitude:
  - "34.176834"
geo_longitude:
  - "-118.789917"
geo_public:
  - "1"
categories:
  - (intro)Spection
  - JavaScript
---
## How to design a (tall JavaScript) function:

Original &#8211; <https://class.coursera.org/programdesign-002/wiki/HtDFModule>

I was watching the video for &#8220;Design a function to determine if an image is tall.&#8221; and using the tall-starter.rkt in DrRacket. As an exercise I transposed it into JavaScript with the following constraints:

  * No libraries
  * Must get a working prototype as fast as possible (10 minutes or less)
  * Test it my own ad hoc way since jasmine/karma/protractor are libraries/frameworks and not native to browsers 
    <!--more-->

##### **Here is a two sentence introduction to JavaScript for the non-programmer:**

> To begin, JavaScript is all about functions and objects.
  
> One way to think about this is to see everything as a function that does stuff and every thing between curly brackets {} as an object or thing that can have stuff done to it.

You see syntax &#8216;var this&#8217; or &#8216;function that&#8217; below. For simple things and exploratory purposes they are ways to tell the JavaScript interpreter what needs to be done and what to do it to. Let&#8217;s get started. I will follow the Design Method defined as part of the htdf module as closely as possible. Open up your web browsers console and type along the statements that follow.

##### **We need an Image. This is just an object and we can create it like this:**

> var Image = function (h,w) {
  
> return {
  
> height: h,
  
> width: w
  
> }
  
> };

Once it is defined I can create new Images and assign them to variables.

> var image = new Image(2, 3);

Now I can make some images to test with later on. You can also enter the var name into the console and click it to print and inspect its object properties.

> var tallImage = new Image(3,2); // { height: 3, width: 2 }
  
> var squareImage = new Image(3,3); // { height: 3, width: 2 }
  
> var shortImage = new Image(2,3); // { height: 2, width: 3 }

##### **Lets design our function that checks if an image is tall.**

We will try to adhere close to the Design Method given in the course. First is the stub, a function called isTall since one cannot use ?&#8217;s in JavaScript function names. All it does is return whatever is given to it. But there are no errors and if you give it one of the objects created above it will give it back to you.

> //Stub -> should run and return whatever it was given
  
> function isTall (img) {
  
> //@In->Out: Image -> Boolean
  
> //@Purpose &#8211; produce true if the image is tall
  
> return img;
  
> }
> 
> isTall(shortImage);    // Returns an object: { height: 2, width: 3 }

Next, we move on to the template, which will give you an error when you type it into the console. Thats ok. Even if it didn&#8217;t give an error it wouldn&#8217;t do much but give us some basic structure.

> // Template -> should error
  
> function isTall (img) {
  
> //@In->Out: Image -> Boolean
  
> //@Purpose &#8211; produce true if the image is tall
  
> if (&#8230;) {
  
> return true;
  
> }
  
> return false;
  
> }

But it does give us an idea for the next step, a prototype that structures our thought around the problem statement. You have a thing with width and height. You need to know when height is less than width, when height is greater than width and when height is the same as width.

> // Prototype One
  
> function isTall (img) {
  
> //@In->Out: Image -> Boolean
  
> //@Purpose &#8211; produce true if the image is tall
  
> if (img.height > img.width) { // first case
  
> return true;
  
> } else if (img.height < img.width) { // second case
  
> return false;
  
> } else if (img.height === img.width) { // third case
  
> return false;
  
> }
  
> }

When we take a moment to think about it, we are returning false for all cases except one. That means we can make it more simple and keep the clues to what it does while not making the next person to read the code think, unless they need to. Deduction tells us that the isTall function can be simplified as follows.

> // Prototype Two
> 
> <span style="line-height: 1.5;">function isTall (img) {</span>
  
> //@In->Out: Image -> Boolean
  
> //@Purpose &#8211; produce true if the image is tall
  
> if (img.height > img.width) {
  
> return true;
  
> }
  
> return false; // Note: the if rule is the only one that satisfies the function statement.
  
> // This means that h < w is short and h === w is false
  
> }

The code reviewer voice in my head is muttering about checking to ensure img is really an image and that is has real numbers set for its height and width attributes but, lets trust that it is for this thought experiment and verify it later. Before this code is pushed to production.

##### **Proving that it works**

> isTall(squareImage)
  
> // false
  
> isTall(shortImage)
  
> // false
  
> isTall(tallImage)
  
> // true

Try it out for yourself. Open the console and type in the functions and statements listed above.