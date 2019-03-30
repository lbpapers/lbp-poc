---
layout: default
title: "World Inquiry"
permalink: /world-inquiry/
nav_order: 470
---
<h1 class="category-title">World Inquiry</h1>
<p>The World Inquiry was prompted by the challenge of the unfinished task of evangelization. The purpose of the “Evangelizing Our World Inquiry” was to further enhance world evangelization in the 21st century by means of a quantitative and qualitative research enquiry using a survey and focus group consultative process to gather, compile, organize and communicate the insights of Christian leaders throughout the world.</p>
<p>The inquiry objectives included seeking to discover the citywide, countrywide, continent-wide and global current realities and the obstacles and opportunities for evangelization. It involved collecting insights, beliefs, and attitudes about issues, leadership and structures related to world evangelization to identify a unifying paradigm of mission which turned out to be mission as transformation which led to the Transform World Movement.</p>
<p>Documents in this section are historical documents, and not up-to-date.</p>
<ul>
  {% for post in site.posts %}
    {% assign category = post.category | downcase %}{% if category == 'world-inquiry' %}
      <li class="article-list">
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><br>
        <div class="author">Author: {{ post.author }}</div>
        <div class="publication-date">Publication Date: <time datetime="{{post.date | date: '%F'}}">{{post.date | date: '%B %d, %Y'}}</time></div>
        <div class="excerpt">{{post.excerpt | strip_html | truncatewords:55 }}</div>
      </li>
    {% endif %}
  {% endfor %}
</ul>
