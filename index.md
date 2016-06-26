---
layout: page
title: Periodical Musings
tagline: Probably!
---
{% include JB/setup %}

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    <span>{{ post.description }}</span>
  {% endfor %}
</ul>



