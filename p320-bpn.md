---
layout: default
title: "BPN"
permalink: /bpn/
nav_order: 320
---
<h1 class="category-title">BNP</h1>

<p>Description</p>

<div class="article-container">
  {% for post in site.posts %}
    {% assign category = post.category | downcase %}{% if category == 'bpn' %}
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
