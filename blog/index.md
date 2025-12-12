---
layout: default
title: Blog
permalink: /blog/
---

# Blog

Welcome to my (occasional) notes on quantum gravity, cosmology,
teaching, and academic life.

<ul class="post-list">
{% for post in site.posts %}
  <li>
    <a href="{{ post.url | relative_url }}"><strong>{{ post.title }}</strong></a><br>
    <span class="post-meta">
      <strong> {{ post.date | date: "%B %-d, %Y" }} </strong>
      {% if post.tags and post.tags != empty %}
        • {{ post.tags | join: ", " }}
      {% endif %}
    </span>
    {% if post.excerpt %}
      <p>{{ post.excerpt | strip_html | truncate: 180 }}</p>
    {% endif %}
  </li>
{% endfor %}
</ul>
