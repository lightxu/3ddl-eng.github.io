---
layout: post
title:  "Setup Jekyll"
date:   2024-08-13
tag:    jekyll
---

Setting up Github Pages + Jekyll is quite straightforward, I am using WSL2 + Ubuntu for installing Jekyll. WSL doesn't open the port 4000 that Jekyll uses by default, instead, port 8080 works. Also, I will need to enable `--force-polling` so that the page gets refreshed when I reload in browser.

Here is the command for local page development.

{% highlight bash %}
bundle exec jekyll serve -P 8080 --force-polling
{% endhighlight %}

For now, let's keep it simple. I adopted the category structure, created a draft folder, and will use tags. I will focus on learning and blogging before tweaking Jekyll more :)

References:
* [Creating a GitHub Pages site with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll)
* [Jekyll on Ubuntu](https://jekyllrb.com/docs/installation/ubuntu/)
* [Jekyll Posts: Tags and Categories](https://jekyllrb.com/docs/posts/#tags-and-categories)
