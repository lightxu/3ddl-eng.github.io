---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

<h3>Latest articles</h3>
{% assign sorted_posts = site.posts | sort: "date" | reverse | slice: 0, 3 %}
<ul>
  {% for post in sorted_posts %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

{% assign sorted_categories = site.categories | sort %}
{% for category in sorted_categories %}
  <h3>{{ category[0] | split: "_" | slice: 1, 100 | join: " " | capitalize }}</h3>
  <ul>
    {% assign sorted_posts = category[1] | sort: "date" %}
    {% for post in sorted_posts %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
