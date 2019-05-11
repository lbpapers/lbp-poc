---
layout: default
title: Newsletters(English)
permalink: /newsletters-english/
nav_order: 1000
---
<h1 class="category-title">Newsletters</h1>

<div class="article-container">
  {% for post in site.posts %}
    {% assign category = post.category | downcase %}{% if post.lang == 'en' and category == 'newsletters' %}
      <div class="article-list">
        <div class="article-category"></div>
        <div class="article-summary">
          <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><br>
          <figure class="author-date">
            <div class="author">{{ post.author }}</div>
            <div class="publication-date"><time datetime="{{post.date | date: '%F'}}">{{post.date | date: '%B %d, %Y'}}</time></div>
          </figure>
          <div class="excerpt">{{post.excerpt | strip_html | truncatewords:55 }}</div>
        </div>
      </div>
    {% endif %}
  {% endfor %} 
</div>
