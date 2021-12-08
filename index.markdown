---
title: Our Drama Museum
layout: index
---

{% for exhibit in site.exhibits %}

{% assign individual = site.data.categories | find: "title", exhibit.title %}
{% assign writers = site.data.writers | find: "writer", exhibit.writer %}

<a href="{{ exhibit.url | relative_url }}" target="_blank" title="跳转到individual page"><img src="{{ exhibit.image-url }}" width = 350></a>
<h3><a href="{{ exhibit.url | relative_url }}">{{ exhibit.title }}</a> by <a href="{{ writers.writer-url }}">{{ exhibit.writer }}</a></h3>
<p>{{ exhibit.short-introduction }}</p>

{% endfor %}