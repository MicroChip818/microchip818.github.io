---
layout: default
title: Homepage
---

Welcome to my coding blog! I explore the vast world of programming and share my discoveries through coding projects and exercises. Let's learn coding together!
## Latest Posts
<ul class="post_list">
  {% for post in site.posts %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% else %}
    <li>No posts yet. Check back soon!</li>
  {% endfor %}
</ul>
