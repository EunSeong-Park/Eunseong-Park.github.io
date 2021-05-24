---
layout: default
title: Home
---

# 박은성 Eunseong Park 

<ul>
{% for post in paginator.posts %}
     <li>{{ post.date | date: '%Y-%m-%d'}} <a href="{{ post.url }}">{{ post.title }}</a></li>    
{% endfor %}
</ul>

<div class="pagination">
  {% if paginator.next_page %}
    <a class="pagination-item older" href="{{ paginator.next_page_path | relative_url }}">Older</a>
  {% else %}
    <span class="pagination-item older">Older</span>
  {% endif %}
  {% if paginator.previous_page %}
    <a class="pagination-item newer" href="{{ paginator.previous_page_path | prepend: relative_url }}">Newer</a>
  {% else %}
    <span class="pagination-item newer">Newer</span>
  {% endif %}
</div>
