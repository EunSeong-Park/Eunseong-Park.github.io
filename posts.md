---
layout: default
title: Posts
---

# Posts


<ul>
{% for post in site.posts %}
  {% if post.title != 'REDIRECT' %}
  <li>{{ post.date | date: '%Y-%m-%d'}} <a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>
