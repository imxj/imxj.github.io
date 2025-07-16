---
layout: default
title: Blog
permalink: /blog/
---
Welcome to my thoughts repository

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <h3>
        <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
        <span class="post-meta"> - {{ post.date | date: "%b %-d, %Y" }}</span>
      </h3>
    </li>
  {% endfor %}
</ul>

{% if site.posts.size == 0 %}
  <p>No posts yet. Check back soon!</p>
{% endif %}