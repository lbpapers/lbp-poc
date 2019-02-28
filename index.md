---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
<h1>proof of concept</h1>
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><br>
      {{post.date | date: '%B %d, %Y'}}<br>
      {{post.excerpt | strip_html | truncatewords:35 }}
    </li>
  {% endfor %}
</ul>
