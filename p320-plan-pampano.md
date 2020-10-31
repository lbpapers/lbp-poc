---
layout: default
title: "Plan Pampano"
permalink: /plan-pampano/
nav_order: 320
---
<h1 class="category-title">Plan Pampano</h1>

<p>Plan Pampano refers to Jesus' Discipleship Branch Plan for new Christians, presented in John 15:1-17, which provided a sound biblical basis for lighting the fires of a disciple-making movement that served as the basis for discipling new believers at the time of the civil war in El Salvador and fueled the emerging Iberoamerican missions movement.</p>

{% assign category = 'plan-pampano' %}{% assign total_documents = site.posts | where: "categories", category | where_exp: "status", "post.status == published" | size %}{% if total_documents == 0 %}
  <figure style="position: fixed; top: 20%; left: 50%; margin-left: -250px; width: 400px;">
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
