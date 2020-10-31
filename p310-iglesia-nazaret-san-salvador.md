---
layout: default
title: "Iglesia Nazaret, San Salvador"
permalink: /iglesia-nazaret-san-salvador/
nav_order: 310
---
<h1 class="category-title">Iglesia Nazaret, San Salvador</h1>

<p><strong>Iglesia Nazaret:</strong> is making disciples from San Salvador, El Salvador to the ends of the earth through her mission outreach to the nations. Iglesia Nazaret founded the Salvadoran Evangelical mission in 1984, hosted the regional mission conference Mision ‘84 and catalyzed COMIBAM ’87 reported by Ralph Winter to be the meeting of the century who wrote: <em>"This meeting represents the first time that the final geographic limits of the earth's surface have provided both representatives and the very initiators of a global level congress focused exclusively on the ‘missionary dimensions’ of world evangelization."</em></p>

{% assign category = 'iglesia-nazaret-san-salvador' %}{% assign total_documents = site.posts | where: "categories", category | where_exp: "status", "post.status == published" | size %}{% if total_documents == 0 %}
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
