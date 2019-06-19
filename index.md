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
<p>Welcome to the <strong>Luis Bush Papers</strong>!<br> Have you ever stopped to ponder where you are and where you are going on life’s journey? For each person there is a pathway forward. My friend Peter Lee challenged me to leave ‘the trail’ for the next generation” which prompted this project. Doris, my dear life partner, and I have twenty grandchildren. Even if this were just for one of them it would be worth the while. I notice that Peter Lee did not challenge me to leave “a trail” but rather to leave “the trail.” Jesus left us “the trail” when he said of himself: “I am the way, the truth and the life” (John 14:6).  Discover “the trail” toward your ultimate destiny by taking one small step forward at a time, leaning on Jesus. <strong>Live life the JESUS Way.</strong></p>
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
