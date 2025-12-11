---
layout: default
title: Talks
permalink: /research/talks/
---

# Talks

<ul>
{% assign talks = site.data.talks | sort: "date" | reverse %}
{% for t in talks %}
  <li>
    <strong>{{ t.title }}</strong><br>
    {{ t.event }} — {{ t.location }} ({{ t.date | date: "%B %-d, %Y" }})
    {% if t.link %}
      • <a href="{{ t.link }}">slides/video</a>
    {% endif %}
  </li>
{% endfor %}
</ul>
