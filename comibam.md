---
layout: default
title: COMIBAM
permalink: /comibam/
---
<h1>COMIBAM</h1>
<ul>
  {% for post in site.posts %}
    {% assign category = post.category | downcase %}{% if category == 'comibam' %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a><br>
        Author: {{ post.author }}<br>
        {{post.date | date: '%B %d, %Y'}}<br>
        {{post.excerpt | strip_html | truncatewords:35 }}
      </li>
    {% endif %}
  {% endfor %}
</ul>
