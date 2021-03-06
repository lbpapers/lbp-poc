---
layout: default
title: Partners International
permalink: /partners-international/
nav_order: 340
---
<h1 class="category-title">Partners International</h1>

<p>Partners International is a nonprofit Christian ministry that works to spread the Gospel and develop communities in unreached countries by partnering with local ministries in the 10/40 Window. PI is building the church in the least reached places by supporting servants of God in the face of persecution. As a member of the Global Partnership Alliance engaged with holistic development organizations serving indigenous Christian leaders to bring sustainable transformation to advance the Kingdom of God.</p>

{% assign category = 'partners-international' %}{% assign total_documents = site.posts | where: "categories", category | where_exp: "status", "post.status == published" | size %}{% if total_documents == 0 %}
  <figure style="position: fixed; top: 35%; left: 50%; margin-left: -250px; width: 400px;">
    <img src="{{ site.baseurl }}/assets/images/luis-and-doris-300px.png" style="display: block; margin: auto"><br>
    <img src="{{ site.baseurl }}/assets/images/staytuned.png" style="display: block; margin: auto">
  </figure>
{% else %}
  <div class="article-container">
  {% assign category_posts = site.posts | where: "categories", category %}
   {% assign sorted_posts = category_posts | sort: 'title' %}{% for post in sorted_posts %}{% if post.status == 'published' %}
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
    {% endif %}{% endfor %}
  </div>
{% endif %}
