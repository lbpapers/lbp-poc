---
layout: default
title: Newsletters(English)
permalink: /newsletters-english/
---
<h1 class="category-title">Newsletters</h1>
<ul>
  {% for post in site.posts %}
    {% if post.lang == 'en' and post.category == 'newsletters' %}
      <li class="article-list">
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><br>
        <div class="author">Author: {{ post.author }}</div>
        <div class="publication-date">Publication Date: <time datetime="{{post.date | date: '%F'}}">{{post.date | date: '%B %d, %Y'}}</time></div>
        <div class="excerpt">{{post.excerpt | strip_html | truncatewords:55 }}</div>
      </li>
    {% endif %}
  {% endfor %}
</ul>
