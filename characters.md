---
layout: default
title: Characters
permalink: /characters/
---

# Characters of the Chronicle

*The players in our tale, as they have been revealed.*

{% assign has_characters = false %}

{% if site.data.story_state.characters.protagonists.size > 0 %}
  {% assign has_characters = true %}
{% endif %}
{% if site.data.story_state.characters.antagonists.size > 0 %}
  {% assign has_characters = true %}
{% endif %}
{% if site.data.story_state.characters.supporting.size > 0 %}
  {% assign has_characters = true %}
{% endif %}

{% if has_characters %}

{% if site.data.story_state.characters.protagonists.size > 0 %}
## Protagonists

<div class="characters-grid">
{% for char in site.data.story_state.characters.protagonists %}
  <div class="character-card">
    <h3>{{ char.name }}</h3>
    <p class="character-role">{{ char.role }}</p>
    <p class="character-description">{{ char.description | strip_newlines | truncate: 300 }}</p>
    <p class="character-status {{ char.status }}">
      {% if char.status == 'alive' %}🟢 Active{% elsif char.status == 'dead' %}💀 Deceased{% else %}❓ Unknown{% endif %}
      {% if char.first_appeared %} · First appeared: Chapter {{ char.first_appeared }}{% endif %}
    </p>
  </div>
{% endfor %}
</div>
{% endif %}

{% if site.data.story_state.characters.antagonists.size > 0 %}
## Antagonists

<div class="characters-grid">
{% for char in site.data.story_state.characters.antagonists %}
  <div class="character-card">
    <h3>{{ char.name }}</h3>
    <p class="character-role">{{ char.role }}</p>
    <p class="character-description">{{ char.description | strip_newlines | truncate: 300 }}</p>
    <p class="character-status {{ char.status }}">
      {% if char.status == 'alive' %}🟢 Active{% elsif char.status == 'dead' %}💀 Deceased{% else %}❓ Unknown{% endif %}
      {% if char.first_appeared %} · First appeared: Chapter {{ char.first_appeared }}{% endif %}
    </p>
  </div>
{% endfor %}
</div>
{% endif %}

{% if site.data.story_state.characters.supporting.size > 0 %}
## Supporting Characters

<div class="characters-grid">
{% for char in site.data.story_state.characters.supporting %}
  <div class="character-card">
    <h3>{{ char.name }}</h3>
    <p class="character-role">{{ char.role }}</p>
    <p class="character-description">{{ char.description | strip_newlines | truncate: 300 }}</p>
    <p class="character-status {{ char.status }}">
      {% if char.status == 'alive' %}🟢 Active{% elsif char.status == 'dead' %}💀 Deceased{% else %}❓ Unknown{% endif %}
      {% if char.first_appeared %} · First appeared: Chapter {{ char.first_appeared }}{% endif %}
    </p>
  </div>
{% endfor %}
</div>
{% endif %}

{% else %}

<p class="tale-intro">
  <em>No characters have been introduced yet. The story awaits its first scene...</em>
</p>

{% endif %}

---

## The World

{% if site.data.story_state.world.name %}
**{{ site.data.story_state.world.name }}** · *{{ site.data.story_state.world.era }}*

{{ site.data.story_state.world.description | strip_newlines }}

{% if site.data.story_state.world.locations.size > 0 %}
### Known Locations

<div class="characters-grid">
{% for loc in site.data.story_state.world.locations %}
  <div class="character-card">
    <h3>{{ loc.name }}</h3>
    <p class="character-description">{{ loc.description }}</p>
  </div>
{% endfor %}
</div>
{% endif %}

{% if site.data.story_state.magic_system %}
### Magic System: {{ site.data.story_state.magic_system.name }}

{{ site.data.story_state.magic_system.description | strip_newlines }}

**Costs:** {{ site.data.story_state.magic_system.costs }}

**Limits:** {{ site.data.story_state.magic_system.limits }}
{% endif %}

{% endif %}
