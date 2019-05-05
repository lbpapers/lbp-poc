---
layout: default
title: "Family and Heritage"
permalink: /family-and-heritage/
nav_order: 110
---
<h1 class="category-title">Family and Heritage</h1>

{% assign category = 'family-and-heritage' %}{% assign total_documents = site.posts | where: "categories", category | size %}{% if total_documents == 0 %}
  <figure style="position: fixed; top: 20%; left: 50%; margin-left: -250px; width: 400px;">
    <img src="{{ site.baseurl }}/assets/images/luis-and-doris-300px.png" style="display: block; margin: auto"><br>
    <img src="{{ site.baseurl }}/assets/images/staytuned.png" style="display: block; margin: auto">
  </figure>
{% else %}
  <p>Description</p>

  <div class="article-container">
  {% assign posts = site.posts | where: "categories", category %}
   {% assign sorted_posts = site.posts | sort: 'title' %}{% for post in sorted_posts %}
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
