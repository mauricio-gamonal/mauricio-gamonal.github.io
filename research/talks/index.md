---
layout: default
title: Talks
permalink: /research/talks/
---

# Talks & presentations

{% assign talks = site.data.talks | sort: "date" | reverse %}
{% assign invited    = talks | where: "type", "invited" %}
{% assign contributed = talks | where: "type", "contributed" %}
{% assign schools    = talks | where: "type", "school" %}

## Invited talks

<ul>
{% for t in invited %}
  <li>
    <strong>{{ t.date | date: "%B %-d, %Y" }}</strong> — 
    {% if t.link %}
      <a href="{{ t.link }}" target="_blank" rel="noopener noreferrer">{{ t.event }}</a>
    {% else %}
      {{ t.event }}
    {% endif %}
    {% if t.location %}
      , {{ t.location }}
    {% endif %}
    {% if t.talk_title %}
      <br><em>"{{ t.talk_title }}"</em>
    {% endif %}
    {% if t.slides or t.video %}
      <br>
      {% if t.slides %}
        <a href="{{ t.slides }}" target="_blank" rel="noopener noreferrer">slides</a>
      {% endif %}
      {% if t.slides and t.video %}
        &nbsp;·&nbsp;
      {% endif %}
      {% if t.video %}
        <a href="{{ t.video }}" target="_blank" rel="noopener noreferrer">video</a>
      {% endif %}
    {% endif %}
  </li>
{% endfor %}
</ul>

## Contributed talks (selected)

<ul>
{% for t in contributed %}
  <li>
    <strong>{{ t.date | date: "%B %-d, %Y" }}</strong> — 
    {% if t.link %}
      <a href="{{ t.link }}" target="_blank" rel="noopener noreferrer">{{ t.event }}</a>
    {% else %}
      {{ t.event }}
    {% endif %}
    {% if t.location %}
      , {{ t.location }}
    {% endif %}
    {% if t.talk_title %}
      <br><em>"{{ t.talk_title }}"</em>
    {% endif %}
    {% if t.slides or t.video %}
      <br>
      {% if t.slides %}
        <a href="{{ t.slides }}" target="_blank" rel="noopener noreferrer">slides</a>
      {% endif %}
      {% if t.slides and t.video %}
        &nbsp;·&nbsp;
      {% endif %}
      {% if t.video %}
        <a href="{{ t.video }}" target="_blank" rel="noopener noreferrer">video</a>
      {% endif %}
    {% endif %}
  </li>
{% endfor %}
</ul>

## Summer schools & workshops (attendance)

<ul>
{% for t in schools %}
  <li>
    <strong>{{ t.date | date: "%B %Y" }}</strong> — 
    {% if t.link %}
      <a href="{{ t.link }}" target="_blank" rel="noopener noreferrer">{{ t.event }}</a>
    {% else %}
      {{ t.event }}
    {% endif %}
    {% if t.location %}
      , {{ t.location }}
    {% endif %}
    {% if t.notes %}
      <br><em>{{ t.notes }}</em>
    {% endif %}
  </li>
{% endfor %}
</ul>
