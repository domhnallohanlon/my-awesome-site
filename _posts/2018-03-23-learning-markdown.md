---
layout: post
title:  "Learning Markdown"
date:   2018-03-23
author: Domhnall
categories: jekyll markdown
---

There are several "flavours" of Markdown, which is a simple and intuitive text formatting language. The more you know the nicer you posts will be.

### Background

In the beginning (2004) there was [John Gruber](https://daringfireball.net/projects/markdown/) who said that Markdown is two things:

>(1) a plain text formatting syntax; and 
>
>(2) a software tool, written in Perl, that converts the plain text formatting to HTML. 

Since there, as with any software project, there have forks and updates and philosphical arguments. 

In Jekyll a markdown engine known as [Kramdown](https://github.com/gettalong/kramdown) is used.

### Headings

In Markdown `#` symbols are used to denote a heading. The more hash symobls you have the lower rank of the heading.

{% highlight markdown %}
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
{% endhighlight%}
### Text

### Links

### Images

### Footnotes

The inspiration behind this post was that I needed to add some citations to my post aobut syntax highlighting. It turns out this is ridiculously easy to do. Thanks Stack Overflow! [^stackoverflow] Creating the footnote is the easy bit:

{% highlight markdown%}
Sentence that requires citation.[^citation]
{% endhighlight %}

Then, the citation itself, which seems to be white-space dependent. Note that in the link below there is no space between the closing square bracket and the colon. Also, the link text can't have any spaces in it.

{% highlight markdown%}
[^citation]: [external-website](https://xkcd.com/285/)
{% endhighlight %}

You can use any words or numbers for your citations and they will automatically be added to your document in numberical order.

#### Footnotes


[^stackoverflow]: [how-to-add-footnotes-to-github-flavoured-markdown](https://stackoverflow.com/questions/25579868/how-to-add-footnotes-to-github-flavoured-markdown)
