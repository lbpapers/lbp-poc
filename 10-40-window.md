---
layout: default
title: "10/40 Window"
permalink: /1040window/
---
<h1 class="category-title">10/40 Window</h1>
<ul>
  {% for post in site.posts %}
    {% assign category = post.category | downcase %}{% if category == '1040window' %}
      <li class="article-list">
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><br>
        <div class="author">Author: {{ post.author }}</div>
        <div class="publication-date">Publication Date: <time datetime="{{post.date | date: '%F'}}">{{post.date | date: '%B %d, %Y'}}</time></div>
        <div class="excerpt">{{post.excerpt | strip_html | truncatewords:55 }}</div>
      </li>
    {% endif %}
  {% endfor %}
</ul>
