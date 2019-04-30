---
layout: default
title: "Joshua Project"
permalink: /joshua-project/
nav_order: 450
---
<h1 class="category-title">Joshua Project</h1>

<p>Joshua project is an unreached people’s research initiative seeking to bring definition to the unfinished tasks of the great commission by highlighting the ethnic people groups of the world that have the least Christian presence in order to stimulate Pioneer church planting movements in their midst to the end that there will be worshipers for the Lord strong from every tribe tongue nation and people.</p>

<div class="article-container">
  {% for post in site.posts %}
    {% assign category = post.category | downcase %}{% if category == 'joshua-project' %}
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
