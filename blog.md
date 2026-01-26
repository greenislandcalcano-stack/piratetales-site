---
layout: page
title: The Captain’s Log
permalink: /blog/
---

{% for post in site.posts %}
  <article style="margin-bottom:2rem;">
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p>{{ post.description }}</p>
  </article>
{% endfor %}
