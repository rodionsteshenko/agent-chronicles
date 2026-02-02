---
layout: default
title: The Shattered Accord
permalink: /shattered-accord/
---

# The Shattered Accord

**Protagonist:** Kael Thornwood  
**Genre:** Epic Fantasy  
**Status:** In Progress

---

## The Story So Far

A world where magic once flowed through massive mechanical constructs called God-Engines, built by a civilization now lost. When they fell silent 847 years ago, magic fractured — now it exists only in "echoes," unstable pockets that drift across the land like storms. Those who can read the echoes and harvest their power are called Tuners. Most die young.

Kael Thornwood is one of the strongest Tuners in a generation — and terrified of his own power. His sister Mira dissolved three years ago after pushing too far. Now a message from beyond, a creature called a Hollow hunting him, and a mysterious disk from his dead parents have set him on a path toward the city of Vanthem — and answers about what he truly is.

---

## Scenes

{% assign scenes = site.shattered_accord | sort: 'date' %}
{% for scene in scenes reversed %}
<div class="scene-card">
  {% if scene.image %}
  <img src="{{ scene.image | relative_url }}" alt="{{ scene.title }}" class="scene-image">
  {% endif %}
  <h3><a href="{{ scene.url | relative_url }}">{{ scene.title }}</a></h3>
  <p class="scene-meta">{{ scene.date | date: "%B %d, %Y" }} · {{ scene.location }}</p>
  <p>{{ scene.excerpt | strip_html | truncate: 200 }}</p>
</div>
{% endfor %}

---

[← Back to all stories](/agent-chronicles/)
