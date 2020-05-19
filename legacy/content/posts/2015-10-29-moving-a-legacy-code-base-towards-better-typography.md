---
id: 6359
title: 'Moving a legacy code base towards better typography &#8230;'
date: 2015-10-29T23:17:58+00:00
author: matth
layout: post
guid: http://hippeelee.com/?p=6359
permalink: /2015/10/29/moving-a-legacy-code-base-towards-better-typography/
categories:
  - (intro)Spection
---
> ###### I think I can use this in my current project. Yay! Simple Little Things.
> 
> `<span class="token comment" spellcheck="true">/* Document level adjustments */</span>` 
> 
> `<span class="token selector">html </span><span class="token punctuation">{</span> <span class="token property">font-size</span><span class="token punctuation">:</span> 17px<span class="token punctuation">;</span> <span class="token punctuation">}</span>` 
> 
> `<span class="token atrule">@media (max-width<span class="token punctuation">:</span> 900px)</span> <span class="token punctuation">{</span>` 
> 
> `<span class="token selector">    html </span><span class="token punctuation">{</span> <span class="token property">font-size</span><span class="token punctuation">:</span> 15px<span class="token punctuation">;</span> <span class="token punctuation">}</span>` 
> 
> `<span class="token punctuation">}</span>` 
> 
> `<span class="token atrule">@media (max-width<span class="token punctuation">:</span> 400px)</span> <span class="token punctuation">{</span>` 
> 
> `<span class="token selector">    html </span><span class="token punctuation">{</span> <span class="token property">font-size</span><span class="token punctuation">:</span> 13px<span class="token punctuation">;</span> <span class="token punctuation">}</span>` 
> 
> `<span class="token punctuation">}</span>` 
> 
> `<span class="token comment" spellcheck="true">/* Modules will scale with document */</span>` 
> 
> `<span class="token selector"><span class="token class">.header</span> </span><span class="token punctuation">{</span> <span class="token property">font-size</span><span class="token punctuation">:</span> 1.5rem<span class="token punctuation">;</span> <span class="token punctuation">}</span>` 
> 
> `<span class="token selector"><span class="token class">.footer</span> </span><span class="token punctuation">{</span> <span class="token property">font-size</span><span class="token punctuation">:</span> 0.75rem<span class="token punctuation">;</span> <span class="token punctuation">}</span>` 
> 
> `<span class="token selector"><span class="token class">.sidebar</span> </span><span class="token punctuation">{</span> <span class="token property">font-size</span><span class="token punctuation">:</span> 0.85rem<span class="token punctuation">;</span> <span class="token punctuation">}</span>` 
> 
> `<span class="token comment" spellcheck="true">/* Type will scale with modules */</span>` 
> 
> `<span class="token selector">h1 </span><span class="token punctuation">{</span> <span class="token property">font-size</span><span class="token punctuation">:</span> 3em<span class="token punctuation">;</span> <span class="token punctuation">}</span>` 
> 
> `<span class="token selector">h2 </span><span class="token punctuation">{</span> <span class="token property">font-size</span><span class="token punctuation">:</span> 2.5em<span class="token punctuation">;</span> <span class="token punctuation">}</span>` 
> 
> `<span class="token selector">h3 </span><span class="token punctuation">{</span> <span class="token property">font-size</span><span class="token punctuation">:</span> 2em<span class="token punctuation">;</span> <span class="token punctuation">}</span>`

From one of the masters: <a href="https://css-tricks.com/rems-ems/" target="_blank">https://css-tricks.com/rems-ems/</a>

And if you are using sass, run

> $ bower install sass-rem -S

on your command line. The -S is a shortcut to save the dependency. now you can generate font-size rems with fallbacks. The project is here: <https://github.com/pierreburel/sass-rem>.