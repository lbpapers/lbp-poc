---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
nav_exclude: true
---
<h1>proof of concept</h1>
<h2>Updated on 2019-03-28 08:33 PDT</h2>
<ul>
  {% for post in site.posts %}
    <li class="article-list">
      <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><br>
      <div class="author">Author: {{ post.author }}</div>
      <div class="publication-date">Publication Date: <time datetime="{{post.date | date: '%F'}}">{{post.date | date: '%B %d, %Y'}}</time></div>
      <div class="excerpt">{{post.excerpt | strip_html | truncatewords:55 }}</div>
    </li>
  {% endfor %}
</ul>
