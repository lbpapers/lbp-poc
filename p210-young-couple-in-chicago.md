---
layout: default
title: "Young Couple in Chicago"
permalink: /young-couple-in-chicago/
nav_order: 210
---
<h1 class="category-title">Young Couple in Chicago</h1>

<p>As we began our life together, while working for a business consulting firm in Chicago, we would meet in our new friends’ high-rise apartment to study the Bible with other young business people. God was giving us a bird’s eye view, not only of the city but also of His kingdom, too. As newly weds, we reflected on the Word of God each morning. On one unforgettable morning, as we meditated on Psalm 1 about taking the right path leading to happiness, we sensed God speaking to us about full-time Christian service.</p>

{% assign category = 'young-couple-in-chicago' %}{% assign total_documents = site.posts | where: "categories", category | where_exp: "status", "post.status == published" | size %}{% if total_documents == 0 %}
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
