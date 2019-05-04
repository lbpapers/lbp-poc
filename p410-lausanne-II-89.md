---
layout: default
title: "Lausanne II '89"
permalink: /lausanne-II-89/
nav_order: 400
---
<h1 class="category-title">Lausanne II '89</h1>
<p>Lausanne II in Manila has played a significant role in a movement which stands for completing the task of world evangelization, for cooperation in that cause and for networking between evangelical leaders in that task with highlighting of the "Resistant Belt" / the 10/40 Window.</p>

{% assign category = 'lausanne-ii-89' %}{% assign total_documents = site.posts | where: "categories", category | size %}{% if total_documents == 0 %}
  <figure style="position: fixed; top: 20%; left: 50%; margin-left: -250px; width: 400px;">
    <img src="{{ site.baseurl }}/assets/images/luis-and-doris-300px.png" style="display: block; margin: auto"><br>
    <img src="{{ site.baseurl }}/assets/images/staytuned.png" style="display: block; margin: auto">
  </figure>
{% else %}
  <div class="article-container">
  {% assign posts = site.posts | where: "categories", category %}
    {% for post in posts %}
      <p>Description</p>

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

<!-- <div class="article-container">
  {% for post in site.posts %}
    {% assign category = post.category | downcase %}{% if category == 'lausanne-II-89' %}
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
</div> -->
