---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
nav_exclude: true
search_exclude: true
---
<div class="introduction">
<figure>
<img src="{{ site.url }}{{ site.baseurl }}/assets/images/Luis_Bush_600px.jpg" alt="Luis Bush" />
</figure>
<p>Luis Bush, born and raised in Latin America is married to Doris with whom he has four children and twenty grandchildren. He is a servant catalyst on God’s missional movements including COMIBAM—a Latin America cross-cultural mission’s movement, AD 2000 & Beyond Movement, toward a church for every people and the gospel for every person; 10/40 Window Movement; North India Harvest Network; MANI—Mobilizing African National Initiatives; 35/45 Turkic Window; Transform World Movement—connecting God’s agents of transformation; 4/14 Window Movement—raising up a new generation of children to transform the world; Transform World 2020—responding to seven mega challenges through seven spheres of cultural influence in ten regions of the world; Nurturer Movement—raising up NextGen to disciple the children; Mission China 2030—sending 20,000 Chinese missionaries by 2030, Back to Jerusalem Movement- a Christian missions movement to send missionaries to all the unreached peoples who live between China and Jerusalem.</p>
</div>
<h1 style="border-top: 1px solid grey; margin-top: 2em; padding-top: 1em;">List of documents</h1>
<h4>Please bear in mind this site is still work in progress</h4>
<p>If you have any question, please email at <a href="mailto:email@luisbushpapers.com">email@luisbushpapers.com</a></p>
<div class="article-container">
  {% assign sorted_posts = site.posts | sort: 'title' %}{% for post in sorted_posts %}{% if post.status == 'published' %}
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
      </div>
    </div>
  {% endif %}{% endfor %}
</div>
