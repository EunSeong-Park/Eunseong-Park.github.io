---
layout: default
title: Archive
---

# Archive

Browse all posts by month and year.

{% assign postsByYearMonth = site.posts | group_by_exp: "post", "post.date | date: '%B %Y'" %}
{% for yearMonth in postsByYearMonth %}
  <ul>
    {% for post in yearMonth.items %}
      <li><a href="{{ post.url }}">{{ post.date | date: '%Y-%M-%D'}} {{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

# Temp

  <ul>
{% for post in site.posts %}
  <li>{{ post.date | date: '%Y-%m-%d'}}<a href="{{ post.url }}"> {{ post.title }}</a></li>
{% endfor %}
  </ul>
