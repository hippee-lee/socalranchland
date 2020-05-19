---
id: 6397
title: Tree Traversals
date: 2016-09-21T14:55:29+00:00
author: matth
layout: post
guid: http://hippeelee.com/?p=6397
permalink: /2016/09/21/tree-traversals/
video_format_choose:
  - youtube
qode_show-sidebar:
  - default
qode_hide-featured-image:
  - 'no'
categories:
  - (intro)Spection
---
I am testing myself on some personal learning topics and here are my Q & A&#8217;s. Underlined words indicate an area I need to investigate and understand better. Study was mainly done [here](https://en.wikipedia.org/wiki/Tree_traversal)

#### WHAT IS TREE TRAVERSAL?

Tree traversal in this context is the programmatic visitation to nodes in a tree. In my mind is a BST with data and left and right pointers. The process that a program uses to visit and perform computation on the trees nodes is tree traversal.

#### WHEN PERFORMING TREE TRAVERSAL WHAT STEPS ARE AVAILABLE FOR THE PROGRAM TO PROCESS ALL NODES?

  1. Answer the question &#8220;Are both of this nodes left and right pointers null?&#8221;
  2. Process the nodes data
  3. Traverse to the left node and repeat
  4. Traverse the right node and repeat

Except for the null check, the steps can be performed in any order.

#### WHAT STRATEGIES EXIST FOR TRAVERSING ALL BST TREE NODES AND HOW DO THEY WORK?

Given the following designations for operations:

  * (N) Process node N
  * (L) recursively traverse the left sub tree
  * (R) recursively traverse the right sub tree

There are four types of traversals:

  1. Post Order traversal when at Node N 
      *  Check if N is empty or null
      * (L) recursively traverse the left subtree and end up back at N
      * (R) recursively traverse the right subtree and end up back at N
      * (N) process the node N
  2. In Order Traversal when at Node N 
      * Check if N is empty or null
      * (L) recursively traverse the left subtree and end up back at N
      * (N) process the node N
      * (R) recursively traverse the right subtree and end up back at N
  3. Pre Order traversal when at Node N 
      * Check if N is empty or null
      * (N) process the node N
      * (L) recursively traverse the left subtree and end up back at N
      * (R) recursively traverse the right subtree and end up back at N
  4. Breadth First Search (BFS) 
      * A strategy that visits each level of a BST, progressively getting deeper and processing each level
      * Implementation is through Queue

#### TYPES OF PROBLEMS

Each traversal strategy is adept at solving certain problems.

##### PRE-ORDER

Can be used to duplicate nodes and edges to make a duplicate binary tree. For expression trees it can be used to make a prefix expression (<span style="text-decoration: underline;">polish notation</span>)

##### IN-ORDER

Binary search trees commonly use in-order traversal. In-order traversal returns the values from the underlying set (in order) according to the <span style="text-decoration: underline;">comparator</span> that that set up the BST.

##### POST-ORDER

Post-order traversal, while deleting or freeing nodes and values, can delete or free an entire binary tree. It can also generate a <span style="text-decoration: underline;">postfix representation</span> of the binary tree.

&nbsp;

###