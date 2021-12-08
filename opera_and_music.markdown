---
title: Opera and Musical Drama
layout: index
---

<ul>
{% assign operas = site.exhibits | where: "category", "opera and musical drama" %}
{% assign title_alphabetical = operas | sort: "title" %}
{% for one in title_alphabetical %}
  <li><a href ="{{ one.url | relative_url }}">{{ one.title }}</a></li>
{% endfor %}
</ul>