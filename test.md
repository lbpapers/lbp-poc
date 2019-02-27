---
layout: home
title: Test
permalink: /test/
---
<h1>test</h1>
<ul>
  {% for post in site.html_pages %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a><br>
      {{post.date | date: '%B %d, %Y'}}<br>
      {{post.excerpt | strip_html | truncatewords:35 }}
    </li>
  {% endfor %}
</ul>
<p>calvin kim</p>
