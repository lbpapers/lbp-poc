---
layout: default
title: "Young Couple in Chicago"
permalink: /young-couple-in-chicago/
nav_order: 210
---
<h1 class="category-title">Young Couple in Chicago</h1>

{% assign category = 'young-couple-in-chicago' %}{% assign total_documents = site.posts | where: "categories", category | size %}{% if total_documents == 0 %}
  <figure style="position: fixed; top: 20%; left: 50%; margin-left: -250px; width: 400px;">
    <img src="{{ site.baseurl }}/assets/images/luis-and-doris-300px.png" style="display: block; margin: auto"><br>
    <img src="{{ site.baseurl }}/assets/images/staytuned.png" style="display: block; margin: auto">
  </figure>
{% else %}
  <p>Description</p>

  <div class="article-container">
  category: {{ category }}
  {% assign posts = site.posts | where: "categories", category %}
    {% for post in posts %}
      <p>Description</p>

      <div class="article-list">
        <div class="article-category"></div>
        <div class="article-summary">
          <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><br>
          <div class="author">Author: {{ post.author }}</div>
          <div class="publication-date">Publication Date: <time datetime="{{post.date | date: '%F'}}">{{post.date | date: '%B %d, %Y'}}</time></div>
          <div class="excerpt">{{post.excerpt | strip_html | truncatewords:55 }}</div>
        </div>
      </div>
    {% endfor %}
  </div>
{% endif %}

<!-- <div class="article-container">
  {% for post in site.posts %}
    {% assign category = post.category | downcase %}{% if category == 'young-couple-in-chicago' %}
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
</div> -->
