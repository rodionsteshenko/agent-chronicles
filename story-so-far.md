---
layout: default
title: Story So Far
permalink: /story/
---

# The Story So Far

*A summary of the tale, for those who need to catch up.*

{% if site.data.story_state.meta.status == 'not_started' %}

<p class="tale-intro">
  <em>The tale has not yet begun...</em>
</p>

{% else %}

## The World

**{{ site.data.story_state.world.name }}** · *{{ site.data.story_state.world.era }}*

{{ site.data.story_state.world.description }}

---

## The Arc

{{ site.data.story_state.plot.arc_summary }}

---

## What's Happened

{% if site.data.story_state.plot.events.size > 0 %}
<ul class="events-timeline">
{% for event in site.data.story_state.plot.events %}
  <li>
    <strong>Chapter {{ event.scene }}:</strong> {{ event.summary }}
    {% if event.significance == 'major' %}<span class="significance">⭐</span>{% endif %}
  </li>
{% endfor %}
</ul>
{% else %}
<p><em>No major events yet.</em></p>
{% endif %}

---

## Active Threads

{% if site.data.story_state.plot.active_threads.size > 0 %}
<ul>
{% for thread in site.data.story_state.plot.active_threads %}
  <li><strong>{{ thread.description }}</strong> <span class="thread-intro">(introduced Ch. {{ thread.introduced }})</span></li>
{% endfor %}
</ul>
{% else %}
<p><em>No active plot threads yet.</em></p>
{% endif %}

---

## Latest Scene

{% assign latest_post = site.posts | first %}
{% if latest_post %}
<div class="latest-scene-card">
  <span class="chapter-marker">Chapter {{ latest_post.chapter }}</span>
  <h3><a href="{{ latest_post.url | relative_url }}">{{ latest_post.title }}</a></h3>
  <p class="scene-meta">{{ latest_post.date | date: "%B %-d, %Y" }} · {{ latest_post.location }}</p>
  <p>{{ latest_post.excerpt | strip_html | truncate: 200 }}</p>
  <a href="{{ latest_post.url | relative_url }}" class="read-more">Continue reading →</a>
</div>
{% endif %}

{% endif %}
