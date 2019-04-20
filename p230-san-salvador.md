---
layout: default
title: "San Salvador"
permalink: /san-salvador/
nav_order: 230
---
<h1 class="category-title">San Salvador</h1>

<p>Description</p>

<div class="article-container">
  {% for post in site.posts %}
    {% assign category = post.category | downcase %}{% if category == 'san-salvador' %}
      <div class="article-list">
        <div class="article-category"></div>
        <div class="article-summary">
          <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><br>
          <div class="author">Author: {{ post.author }}</div>
          <div class="publication-date">Publication Date: <time datetime="{{post.date | date: '%F'}}">{{post.date | date: '%B %d, %Y'}}</time></div>
          <div class="excerpt">{{post.excerpt | strip_html | truncatewords:55 }}</div>
        </div>
      </div>
    {% endif %}
  {% endfor %}
</div>
