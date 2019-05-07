---
layout: home
title: Test
permalink: /test/
nav_order: 99999
nav_exclude: true
---
<h1>nav_order - Title - category</h1>
<ul>
  {% for post in site.html_pages %}
    <li>
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.nav_order }} - {{ post.title }} - {{ site.baseurl }}{{ post.url }}</a><br>
      {{post.date | date: '%B %d, %Y'}}<br>
      {{post.excerpt | strip_html | truncatewords:35 }}
    </li>
  {% endfor %}
</ul>
<p>calvin kim</p>

<P>
{% for post in site.html_pages %}
{{post.url | remove: "/"}}: "{{post.title}}"<br>
{% endfor %}
</p>
