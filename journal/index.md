---
layout: page
title: Journal
---
# Journal

<ul>
{% for post in site.posts %}
  <li><span class="entry-date">{{ post.date | date: "%B %-d, %Y" }}</span> - <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
