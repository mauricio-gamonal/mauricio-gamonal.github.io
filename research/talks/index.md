---
layout: default
title: Talks
---

# Invited Talks

<ul>
{% for talk in site.data.talks.invited %}
  <li>
    {% if talk.link %}
      <a href="{{ talk.link }}" target="_blank">{{ talk.title }}</a>
    {% else %}
      {{ talk.title }}
    {% endif %}
    — {{ talk.location }} ({{ talk.date | date: "%B %Y" }})
  </li>
{% endfor %}
</ul>

# Contributed Talks
<ul>
{% for talk in site.data.talks.contributed %}
  <li>
    {% if talk.link %}
      <a href="{{ talk.link }}" target="_blank">{{ talk.title }}</a>
    {% else %}
      {{ talk.title }}
    {% endif %}
    — {{ talk.location }} ({{ talk.date | date: "%B %Y" }})
  </li>
{% endfor %}
</ul>

# Summer Schools & Workshops
<ul>
{% for talk in site.data.talks.schools %}
  <li>
    {% if talk.link %}
      <a href="{{ talk.link }}" target="_blank">{{ talk.title }}</a>
    {% else %}
      {{ talk.title }}
    {% endif %}
    — {{ talk.location }} ({{ talk.date | date: "%B %Y" }})
  </li>
{% endfor %}
</ul>
