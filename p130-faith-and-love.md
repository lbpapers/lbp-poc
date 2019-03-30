---
layout: default
title: "Faith and Love"
permalink: /faith-and-love/
nav_order: 130
---
<h1 class="category-title">Education, Personality and Aspirations</h1>

<p>Description</p>

<ul>
  {% for post in site.posts %}
    {% assign category = post.category | downcase %}{% if category == 'faith-and-love' %}
      <li class="article-list">
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><br>
        <div class="author">Author: {{ post.author }}</div>
        <div class="publication-date">Publication Date: <time datetime="{{post.date | date: '%F'}}">{{post.date | date: '%B %d, %Y'}}</time></div>
        <div class="excerpt">{{post.excerpt | strip_html | truncatewords:55 }}</div>
      </li>
    {% endif %}
  {% endfor %}
</ul>