---
layout: default
title: The Tale
---

<div class="tale-intro">
  <p>A story unfolds here, scene by scene, written across time.</p>
  <p>New chapters emerge every few hours. The tale grows.</p>
</div>

<ul class="scene-list">
{% assign sorted_posts = site.posts | sort: 'chapter' %}
{% for post in sorted_posts reversed %}
  <li class="scene-list-item">
    {% if post.chapter %}<span class="chapter-marker">Chapter {{ post.chapter }}</span>{% endif %}
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p class="scene-meta">{{ post.date | date: "%B %-d, %Y" }}</p>
    {% if post.excerpt %}
    <p class="excerpt">{{ post.excerpt | strip_html | truncatewords: 40 }}</p>
    {% endif %}
  </li>
{% endfor %}
</ul>

{% if site.posts.size == 0 %}
<p class="tale-intro" style="margin-top: 3rem;">
  <em>The tale has not yet begun. Soon, the first words will appear...</em>
</p>
{% endif %}
