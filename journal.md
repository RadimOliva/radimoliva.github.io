---
layout: page
title: Journal
---
# Journal

<ul>
{% for post in site.posts %}
  {% unless post.is_project %}
    <li>{{ post.date | date: "%B %-d, %Y" }} - <a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endunless %}
{% endfor %}
</ul>
