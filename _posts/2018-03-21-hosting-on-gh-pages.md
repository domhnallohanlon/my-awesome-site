---
layout: post
title:  "Hosting on Github Pages"
date:   2018-03-20
author: Domhnall
categories: jekyll gh-pages
---

Now that I've got my head around the structure and capabilities of Jekyll, it's time to commit all this new information to Github. What could possi-blye go wrong?

### Start with the end in Mind

The entire idea of this project was to get better at using Jekyll and to post my discoveries/ramblings in chronoligical order. Easier said than done.

![What could possi-blye go wrong?](https://frinkiac.com/meme/S06E04/443325.jpg?b64lines=IFRoZSBhbXVzZW1lbnQgcGFyayBvZiB0aGUKIGZ1dHVyZSB3aGVyZSBub3RoaW5nIGNhbgogcG9zc2ktYmx5ZSBnbyB3cm9uZy4KIFBvc3NpYmx5IGdvIHdyb25nLg==){:width="50%"}

In order to get this specific post hosted on this specific domain there are a few non-obvious changes needed to get everything up and running.

### TL;DR

It turns out that when working with Jekyll it assumes that you're hosing somewhere other than Github (a fair assumption) and if you tell it that you *are* using Github pages then it assumes that your project live at the root of your domain. (This makes sense too - once you know about it.) To successfully host your site using Github Pages you need to modify the following two files.


### Modify Your Gemfile

To configure Jekyll to run on Github pages you basically just swap two gems that are already in the `Gemfile`. All you need to do is comment out the jekyll gem and uncomment the github-pages gem. Once this is done simply run the following in your terminal and step 1 is complete:

{% highlight shell %}
  bundle update
{% endhighlight %}

All of this information (and more) is contained and well documented over on Github's help pages:

[Setting up your GitHub Pages site locally with Jekyll](https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/#step-4-build-your-local-jekyll-site)

### Set Your Baseurl

Once this is all set up correctly then you need to go into the `_config.yml` file and change the base url:

{% highlight yaml %}
  baseurl: "/my-awesome-site"
{% endhighlight %}

If you're not familiar with github pages, the default URL you get is in the format *username.github.io*. With some minor changes to CNAME and ANAME records you can redirect this to any TLD you own, i.e *yourdomain.com* which is actually what this site does [domhnallohanlon.com](http://domhnallohanlon.com). 
Since this is a side project I created a new repository to keep track of everything. Doing this creates a new website at *username.github.io/project_name* so this is where the need for the **baseurl** property comes from.

Thanks for Parker Moore for clearly explaining how this came about and why it's necessary.

[Clearing Up Confusion Around baseurl](https://byparker.com/blog/2014/clearing-up-confusion-around-baseurl/)


### Print This Page

<a href="https://gitprint.com/domhnallohanlon/my-awesome-site/blob/master/_posts/2018-03-21-hosting-on-gh-pages.md" target="_blank">Print</a>

This is just an experiment with [GitPrint](http://gitprint.com/)