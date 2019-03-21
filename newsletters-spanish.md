---
layout: default
title: Newsletters(Español)
permalink: /newsletters-spanish/
---
<h1>Newsletters (Español)</h1>
<ul>
  {% for post in site.posts %}
    {% if post.lang == 'es' and post.category == 'newsletters' %}
      <li>
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><br>
        {{post.date | date: '%B %d, %Y'}}<br>
        {{post.excerpt | strip_html | truncatewords:35 }}
      </li>
    {% endif %}
  {% endfor %}
</ul>
