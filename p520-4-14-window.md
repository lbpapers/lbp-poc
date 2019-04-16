---
layout: default
title: "4/14 Window"
permalink: /414window/
nav_order: 520
---
<h1 class="category-title">4/14 Window Movement</h1>

<p>The 4/14 Window refers to the demographic group ages 4 to 14, which is the most open and receptive group to spiritual and developmental input. God is calling us to a new missional focus: the 4/14 Window, the golden age of opportunity to transform the world. God is also calling us to radically change the way we view children and to respond to their strategic importance and rightful place in His kingdom. This often-ignored and suffering people group can be transformed into a precious window of opportunity.</p>
<p>The 4/14 Window Movement is a Global Mission Movement focusing on Reaching, Rescuing, Rooting, and Releasing children and youth (0-18 years old) to reach their full transformational impact in their family, community, and nation.</p>

<ul class="article-container">
  {% for post in site.posts %}
    {% assign category = post.category | downcase %}{% if category == '414window' %}
      <li class="article-list">
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><br>
        <div class="author">Author: {{ post.author }}</div>
        <div class="publication-date">Publication Date: <time datetime="{{post.date | date: '%F'}}">{{post.date | date: '%B %d, %Y'}}</time></div>
        <div class="excerpt">{{post.excerpt | strip_html | truncatewords:55 }}</div>
      </li>
    {% endif %}
  {% endfor %}
</ul>
