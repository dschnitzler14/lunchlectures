---
layout: page
title: Past Lectures
permalink: /past-lectures/
---

Feel free to browse our past lectures. Recordings are available for all lectures (unless otherwise stated), however the discussions remain private and are not available for viewing.

<ul>
{% assign curDate = site.time | date: '%Y-%m-%d' %}
  {% for post in site.posts %}
  {% assign postStartDate = post.date | date: '%Y-%m-%d' %}
    {% if postStartDate < curDate %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <span>{{ post.date | date: "%B %d, %Y" }}</span>
    </li>
    {% endif %}
  {% endfor %}
</ul>