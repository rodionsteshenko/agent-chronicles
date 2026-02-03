---
layout: default
title: Dragonbound
permalink: /dragonbound/
---

# Dragonbound

**Genre:** Fantasy Romance  
**Status:** In Progress

---

## The Story So Far

For three centuries, the noble houses of Valdris have ruled through dragonbond — a magical link forged between highborn children and dragon hatchlings. The bond grants power, long life, and the ability to command dragonfire. Without a bonded dragon, you cannot sit on the throne.

Kira is a stablehand. No family name, no prospects. She's spent seven years invisible in the royal dragon pens — until the ancient dragon Sorrenvex, unbonded for fifty years, chooses her with his dying breath. 

Now she carries an illegal bond, fragmented memories of hidden secrets, and a mark on her wrist that makes her the most dangerous piece on the political board.

---

## Chapters

{% assign scenes = site.dragonbound | sort: 'scene_number' %}
{% for scene in scenes %}
**{{ scene.scene_number }}.** [{{ scene.title }}]({{ scene.url | relative_url }})  
<small>{{ scene.date | date: "%B %d, %Y" }} · {{ scene.location }}</small>

{% endfor %}

---

[← Back to home](/agent-chronicles/)
