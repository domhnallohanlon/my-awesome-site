---
layout: post
title:  "Learning Markdown"
date:   2018-03-23
author: Domhnall
categories: jekyll markdown
---

There are several "flavours" of Markdown, which is a simple and intuitive text formatting language. The more you know the nicer your posts will be.

### Background

In the beginning (2004) there was [John Gruber](https://daringfireball.net/projects/markdown/) who said that Markdown is two things:

>(1) a plain text formatting syntax; and 
>
>(2) a software tool, written in Perl, that converts the plain text formatting to HTML. 

Since then, as with any software project, there have been many forks and updates and philosphical arguments. At the moment Jekyll uses a markdown engine known as [Kramdown](https://github.com/gettalong/kramdown) is used.

There are lots of much better[^cheatsheet] [^quickref] references available, but since you're here already feel free to take a look at my summary of Markdown syntax

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

Anything you word processor can do, Markdown can do just as well. In the following table you'll find some examples of the various types of text formatting effects that you can achieve, and how to produce them.

Attribute 	| Markdown Syntax 	| Example
------------|-------------------|--------
Bold				|	`**Doctor**`			| **Doctor**
Bold				| `__Jekyll__` 			| __Jekyll__
Italic			| `*Mister*`				| *Mister*
Italic			| `_Hyde_`					| _Hyde_
Strikethrough|`~~Robert~~`			| ~~Robert~~
Blockquote	| `>Louis`					| n/a
Code				| `` `Stevenson` ``	| `Stevenson`

### Links

#### External Links

If you're familiar with HTML then links might be a bit counter-intuitive. To create a link to an external website, you start by placing the link text in square brackets and then place the href in parentheises.

{% highlight markdown %}

[Just Goolge It](https://google.com)

{% endhighlight%}

The above example produces the following link:

[Just Goolge It](https://google.com)

Note that by  default these links do not open in new tabs.


#### Internal Links

If you want to use internal links (named anchors) in your document you can use a link as normal: 

{% highlight markdown %}

[Footnotes](#footnotes)

{% endhighlight%}

Everytime that you create a heading in your document, Jekyll will automatically apply a "downcased" verion of your heading names as the id. If there are spaces in your heading they are replaced by hyphens.

{% highlight markdown %} ### Adding Footnotes {% endhighlight%}

{% highlight html%} <h3 id="adding-footnotes"></h3> {% endhighlight%}


It is possible to internally link to sections that are not headings, but you then need to add the appropriate block level attribute manually in your markdown.
{: id="manual_links"}

{% highlight markdown%}
** My Definition ** {: id="definition"}
{% endhighlight%}

With both of these elements added to you page you can now add an internal link such as the following:

[Footnotes](#adding-footnotes)

### Lists

There are three different types of lists in Markdown:

- Ordered Lists
- Unordered Lists
- Definition Lists

To create an ordered list you can use the following syntax:

{% highlight markdown%}
1. First
2. Second
3. Third
{% endhighlight%}

Using this formatting will produce the following list:

1. First
2. Second
3. Third

For items that are listed in no particular order you can use an unordered list. Each bullet can be created with any of the following characters:

- `*`
- `+`
- `-` 

{% highlight markdown%}
- Red
+ Green
* Blue
{% endhighlight%}

This will produce the following bulleted list:

- Red
+ Green
* Blue

Finally, definition lists are used to match definitions to their corresponding terms;

{% highlight markdown%}
Jekyll
: Simple, blog-aware, static sites

Markdown
: Lightweight markup langague with plain text formatting.
{% endhighlight%}

Jekyll
: Simple, blog-aware, static sites

Markdown
: Lightweight markup langague with plain text formatting.

### Images

### Adding Footnotes

The inspiration behind this post was that I needed to add some citations to my post aobut syntax highlighting. It turns out this is ridiculously easy to do. Thanks Stack Overflow! [^stackoverflow] Creating the footnote is the easy bit:

{% highlight markdown%}
Sentence that requires citation.[^citation]
{% endhighlight %}

Then, the citation itself, which seems to be white-space dependent. Note that in the link below there is no space between the closing square bracket and the colon. Also, the link text can't have any spaces in it.

{% highlight markdown%}
[^citation]: [external-website](https://xkcd.com/285/)
{% endhighlight %}

You can use any words or numbers for your citations and they will automatically be added to your document in numberical order.

It is also possible to create internal links using [headings](#internal-links) or by appling IDs [manually](#manual_links)

#### Footnotes


[^stackoverflow]: [how-to-add-footnotes-to-github-flavoured-markdown](https://stackoverflow.com/questions/25579868/how-to-add-footnotes-to-github-flavoured-markdown)

[^cheatsheet]: [Markdown-cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

[^quickref]: [KramdownQuickRef](https://kramdown.gettalong.org/quickref.html)
