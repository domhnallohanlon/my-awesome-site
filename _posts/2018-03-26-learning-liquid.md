---
layout: post
title: "A Quick Look at Liquid"
date: 2018-03-26
author: Domhnall
categories: jekyll liquid
---

Liquid is a simple yet powerful templating language that is used by Jekyll to make updates and maintenance much easier.

### What is Liquid

It's one thing to know that Jekyll uses Liquid to programmatically insert data into your site at build-time, but it's another thing altogether to know what liquid actaully is. According to their own webiste[^liquid]:

>Liquid is an open-source template language created by Shopify and written in Ruby. 
>It is the backbone of Shopify themes and is used to load dynamic content on storefronts.

So, sort of like PHP or Ruby itself, liquid can be used to fetch data from a server, insert into a website and serve it to a  browser. Just like [Rouge]({{site.baseurl}}{% link _posts/2018-03-03-syntax-highlighting.md %}), Liquid is also written in Ruby, which presumably means that it's a lot easier to get everything to play nicely together.

### Syntax

### Videos

Shopify partners have a great video that makes learning the fundamentals really straightforward. Take a look for yourself here:

<iframe width="560" height="315" src="https://www.youtube.com/embed/-ihFPNcSkT4" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>


#### Footnotes

[^liquid]:[shopify.github.io](http://shopify.github.io/liquid/)