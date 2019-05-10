---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
nav_exclude: true
updated_on: 2019-05-07T11:56:53-07:00
---
<h1 style="border-top: 1px solid grey; margin-top: 2em; padding-top: 1em;">Work in Progress</h1>
<h4><strong>Documents in this section are not part of main, and should not be shared outside of working group.</strong></h4>
<p>If you have any question, please email at <a href="mailto:email@luisbushpapers.com">email@luisbushpapers.com</a></p>

<div class="article-container">
{% assign sorted_posts = site.posts | sort: 'updated_on' | reverse %}{% for post in sorted_posts %}
    {% if post.status == 'wip' %}
      <div class="article-list">
        <div class="article-category">
          {% if post.lang != 'en' %}{% for language in site.data.language-labels %}{% if language.name == post.lang %}<div class="language-indicator {{language.css-label}}">{{language.label}}</div>{% endif %}{% endfor %}{% endif %}
          {% for cat-label in site.data.category-labels %}{% if cat-label.name == post.category %}<strong>{{ cat-label.label }}</strong>{% endif %}{% endfor %}
        </div>
        <div class="article-summary">
          <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a><br>
          <figure class="author-date">
            <div class="author">{{ post.author }}</div>
            <div class="publication-date"><time datetime="{{post.date | date: '%F'}}">{{post.date | date: '%B %d, %Y'}}</time></div>
          </figure>
          <div class="excerpt">{{post.excerpt | strip_html | truncatewords:55 }}</div>
          <div style="color: #900000; font-size: 65%; border-top: 1px solid black; margin-top: 2em; padding-top: .5em;"><strong>Updated on:</strong> {{ post.updated_on | date: '%B %d, %Y %T %Z' }}</div>
        </div>
      </div>
    {% endif %}
  {% endfor %}
</div>
