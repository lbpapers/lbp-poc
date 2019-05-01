---
layout: default
title: "GCOWE '95 and '97"
permalink: /gcowe/
nav_order: 460
---
<h1 class="category-title">GCOWE '95 and '97</h1>
<h3>Global Consultation On World Evangelization</h3>
<p>GCOWE '95 - a Global Consultation on World Evangelization with more than 3300 delegates from 186 countries committing to and planning to meet the goal of "A Church for Every People, and the Gospel for Every Person by the year 2000."</p>
<p>GCOWE '97 - consisting of ten separate consultations meeting in South Africa beginning with the Mission Executives Consultation with 500 mission agency leaders & the African National Inititaives Consulation with launched MANI(The Movement for African National Initiatives.</p>
<p>MANI is a network of networks focused on catalyzing African National Initiatives and mobilizing the resources of of the Body of Christ in Africa for the fulfillment of the Great Commission.</p>

<div class="article-container">
  {% for post in site.posts %}
    {% assign category = post.category | downcase %}{% if category == 'gcowe' %}
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
