---
layout: default
title: COMIBAM
permalink: /comibam/
nav_order: 350
---
<h1 class="category-title">COMIBAM</h1>
<p>COMIBAM is an alliance that brings together national mission groups and networks in the Ibero-American countries, including Spain, Portugal and Hispanics from the United States and Canada. The vision of COMIBAM is to see the Iberoamerican church as a missionary force capable of taking the Gospel of Jesus Christ to every nation.</p>

<div class="article-container">
 {% assign sorted_posts = site.posts | sort: 'title' %}{% for post in sorted_posts %}
    {% assign category = post.category | downcase %}{% if category == 'comibam' %}
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
