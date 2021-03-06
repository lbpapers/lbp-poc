---
layout: default
title: "Call to San Salvador"
permalink: /call-to-san-salvador/
nav_order: 230
---
<h1 class="category-title">Call to San Salvador</h1>

<p>Our call to San Salvador came on the day of graduation from Dallas Theological Seminary in the form of a letter from Iglesia Nazaret in El Salvador. At the same time, I was invited to pastor the church in São Paulo, where Doris and I had made our decision for Christ. After prayerfully considering the decision, we had an undeniable sense that God was girding up the loins of our minds in preparation for an adventure, calling us to be sober-minded, setting our hope fully upon the grace being brought to us in the revelation of Jesus Christ, and leading us to a place where we did not have roots, to the only nation in the world called: "The Savior"(1 Peter 1:13).</p>

{% assign category = 'call-to-san-salvador' %}{% assign total_documents = site.posts | where: "categories", category | where_exp: "status", "post.status == published" | size %}{% if total_documents == 0 %}
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
