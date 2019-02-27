---
layout: default
title: Newsletters(English)
permalink: /newsletters-english/
---
<h1>Newsletters</h1>
<ul>
  {% for post in site.posts %}
    {% if post.lang == 'en' %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a><br>
        {{post.date | date: '%B %d, %Y'}}<br>
        {{post.excerpt | strip_html | truncatewords:35 }}
      </li>
    {% endif %}
  {% endfor %}
</ul>
