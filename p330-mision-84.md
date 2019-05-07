---
layout: default
title: "Mision 84"
permalink: /mision84/
nav_order: 330
---
<h1 class="category-title">Mision 84</h1>

<p>Mision '84 a mission conference with 1,000 participants hosted by Iglesia Nazaret in San Salvador from eleven Latin American countries during the height of the civil war in El Salvador led to the founding of the first Salvadoran cross-cultural interdenominational missionary agency called MIES which means Harvest. It provided an opportunity to assess the interest in a continent-wide mission conference and led to COMIBAM '87 convened in Sao Paulo, Brazil, more than 3,100 church leaders gathered to listen to a clear and convincing Macedonian call.</p>

{% assign category = 'mision84' %}{% assign total_documents = site.posts | where: "categories", category | size %}{% if total_documents == 0 %}
  <figure style="position: fixed; top: 20%; left: 50%; margin-left: -250px; width: 400px;">
    <img src="{{ site.baseurl }}/assets/images/luis-and-doris-300px.png" style="display: block; margin: auto"><br>
    <img src="{{ site.baseurl }}/assets/images/staytuned.png" style="display: block; margin: auto">
  </figure>
{% else %}
  <div class="article-container">
  {% assign category_posts = site.posts | where: "categories", category %}
   {% assign sorted_posts = category_posts | sort: 'title' %}{% for post in sorted_posts %}
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
    {% endfor %}
  </div>
{% endif %}
