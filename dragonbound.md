---
layout: default
title: Dragonbound
permalink: /dragonbound/
---

# Dragonbound

**Protagonist:** Kira  
**Genre:** Fantasy Romance  
**Status:** In Progress

---

## The Story So Far

For three centuries, the noble houses of Valdris have ruled through dragonbond — a magical link forged between highborn children and dragon hatchlings. The bond grants power, long life, and the ability to command dragonfire. Without a bonded dragon, you cannot sit on the throne.

Kira is a stablehand. No family name, no prospects. She's spent seven years invisible in the royal dragon pens — until the ancient dragon Sorrenvex, unbonded for fifty years, chooses her with his dying breath. 

Now she carries an illegal bond, fragmented memories of hidden secrets, and a mark on her wrist that makes her the most dangerous piece on the political board. Two princes have taken notice. The succession crisis has a new player. And somewhere, hidden eggs wait for someone to find them.

---

## Scenes

{% assign scenes = site.dragonbound | sort: 'date' %}
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
