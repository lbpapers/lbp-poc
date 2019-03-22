---
layout: home
title: Test
permalink: /test/
nav_order: 99999
---
<h1>this is test page</h1>
<ul>
  {% for post in site.html_pages %}
    <li>
      <a href="{{ post.url }}">{{ post.title }} - {{ post.url }}</a><br>
      {{post.date | date: '%B %d, %Y'}}<br>
      {{post.excerpt | strip_html | truncatewords:35 }}
    </li>
  {% endfor %}
</ul>
<p>calvin kim</p>
