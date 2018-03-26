---
layout: post
title: "How does Syntax Highlighting work in Jekyll?"
date: 2018-03-03
categories: jekyll tutorial
permalink: /syntax_highlighting/
---

With the introduction of Jekyll 3 syntax highlighting for over ~~60~~ 100 programming languages is supported thanks to Rouge

### What is Rouge?
According to their own website, Rouge[^Rouge] is a code highlighter written in Ruby. Older version of Jekyll have used a different code highlighter called Redcarpet. This is a great piece of software but since it's written in Python and Jekyll is written in Ruby my understanding is that there were issues with optimisation/compile times for the static site generator. Moving to a highlighter written in Ruby mitigates many of these issues. 


### A Note on Pygments

### Stylesheets


#### External Resources

[CSS Generator](http://jwarby.github.io/jekyll-pygments-themes/languages/javascript.html)

#### Footnotes

[^Rouge]: [Rouge](http://rouge.jneen.net/)