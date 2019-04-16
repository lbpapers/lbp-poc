---
layout: default
title: "San Salvador"
permalink: /san-salvador/
nav_order: 230
---
<h1 class="category-title">San Salvador</h1>

<p>Description</p>

<ul class="article-container">
  {% for post in site.posts %}
    {% assign category = post.category | downcase %}{% if category == 'san-salvador' %}
      <li class="article-list">
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><br>
        <div class="author">Author: {{ post.author }}</div>
        <div class="publication-date">Publication Date: <time datetime="{{post.date | date: '%F'}}">{{post.date | date: '%B %d, %Y'}}</time></div>
        <div class="excerpt">{{post.excerpt | strip_html | truncatewords:55 }}</div>
      </li>
    {% endif %}
  {% endfor %}
</ul>
