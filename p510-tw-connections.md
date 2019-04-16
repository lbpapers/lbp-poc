---
layout: default
title: "TW Connections"
permalink: /tw-connections/
nav_order: 420
---
<h1 class="category-title">Transform Word Connections</h1>
<p>Transform World Connections(TWC) is to catalyze and connect God’s servants for the purpose of co- laboring in the geographic area where they live in a tri-generational initiative in their respective spheres or domains of cultural influence on God’s mission of transformation resulting in a transformational movement in response to the mega challenges of our day in an effort to define a comprehensive approach to transformation “rooted in the theology of the mission of the Kingdom of God that seeks to express the Lordship of Christ over every aspect of life, economic, religious, personal, and political.</p>
<ul class="article-container">
  {% for post in site.posts %}
    {% assign category = post.category | downcase %}{% if category == 'tw-connections' %}
      <li class="article-list">
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><br>
        <div class="author">Author: {{ post.author }}</div>
        <div class="publication-date">Publication Date: <time datetime="{{post.date | date: '%F'}}">{{post.date | date: '%B %d, %Y'}}</time></div>
        <div class="excerpt">{{post.excerpt | strip_html | truncatewords:55 }}</div>
      </li>
    {% endif %}
  {% endfor %}
</ul>
