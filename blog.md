---
layout: blog 
title: "Blog"
permalink: /blog
date: 2018-05-23
modified: 2018-05-23
share: false
ads: false
---
  {% for post in site.posts %}
  <a href="{{ site.github.url }}{{ post.url }}" title="{{ post.title }}" class="post-teaser">{% if post.image.teaser %}<img src="{{ site.github.url }}/images/{{ post.image.teaser }}" alt="teaser" itemprop="image">{% endif %}</a>
  {% if post.date %}<p class="entry-date date published"><time datetime="{{ post.date | date: "%Y-%m-%d" }}" itemprop="datePublished">{{ post.date | date: "%B %d, %Y" }}</time></p>{% endif %}
  <h2 class="post-title" itemprop="name"><a href="{{ site.github.url }}{{ post.url }}">{{ post.title }}</a></h2>
  <p class="post-excerpt" itemprop="description">{{ post.excerpt | strip_html | truncate: 160 }}</p>

  {% endfor %}
