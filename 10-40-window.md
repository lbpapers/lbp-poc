---
layout: default
title: "10/40 Window"
permalink: /1040window/
---
<h1>10/40 Window</h1>
<ul>
  {% for post in site.posts %}
    {% assign category = post.category | downcase %}{% if category == '1040window' %}
      <li>
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><br>
        Author: {{ post.author }}<br>
        {{post.date | date: '%B %d, %Y'}}<br>
        {{post.excerpt | strip_html | truncatewords:35 }}
      </li>
    {% endif %}
  {% endfor %}
</ul>
