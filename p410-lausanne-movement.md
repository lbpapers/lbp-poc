---
layout: default
title: "Lausanne Movement"
permalink: /lausanne-movement/
nav_order: 400
---
<h1 class="category-title">Lausanne Movement</h1>
<p>Description</p>
<ul>
  {% for post in site.posts %}
    {% assign category = post.category | downcase %}{% if category == 'lausanne' %}
      <li class="article-list">
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><br>
        <div class="author">Author: {{ post.author }}</div>
        <div class="publication-date">Publication Date: <time datetime="{{post.date | date: '%F'}}">{{post.date | date: '%B %d, %Y'}}</time></div>
        <div class="excerpt">{{post.excerpt | strip_html | truncatewords:55 }}</div>
      </li>
    {% endif %}
  {% endfor %}
</ul>
