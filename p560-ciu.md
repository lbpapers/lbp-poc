---
layout: default
title: "Cornerstone International University"
permalink: /ciu/
nav_order: 560
---
<h1 class="category-title">Cornerstone International University</h1>
<p>CIU exists to train church leaders in North Korea and house church leaders in China on how to minister effectively to the local church in their communities.</p>

{% assign category = 'lausanne-ii-89' %}{% assign total_documents = site.posts | where: "categories", category | where_exp: "status", "post.status == published" | size %}{% if total_documents == 0 %}
  <figure style="position: fixed; top: 20%; left: 50%; margin-left: -250px; width: 400px;">
    <img src="{{ site.baseurl }}/assets/images/luis-and-doris-300px.png" style="display: block; margin: auto"><br>
    <img src="{{ site.baseurl }}/assets/images/staytuned.png" style="display: block; margin: auto">
  </figure>
{% else %}
  <div class="article-container">
  {% assign category_posts = site.posts | where: "categories", category %}
   {% assign sorted_posts = site.posts | sort: 'title' %}{% for post in sorted_posts %}
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
    {% endfor %}
  </div>
{% endif %}
