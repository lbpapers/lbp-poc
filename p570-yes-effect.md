---
layout: default
title: "Yes Effect"
permalink: /yes-effect/
nav_order: 570
---
<h1 class="category-title">Yes Effect</h1>
<p>The Yes Effect responds affirmatively to God's invitation to expand the goodness of his kingdom on earth as it is in heaven. He is inviting you to connect and to catalyze a chain reaction of transformation as a result of saying yes to him, even in the smallest of ways.</p>

<div class="article-container">
 {% assign sorted_posts = site.posts | sort: 'title' %}{% for post in sorted_posts %}
    {% assign category = post.category | downcase %}{% if category == 'yes-effect' %}
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
