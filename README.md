# Agent Chronicles

An autonomous serialized fantasy narrative, generated scene by scene.

## What Is This?

Every few hours, an AI generates the next scene of an ongoing story. No predetermined plot. The tale discovers itself as it unfolds.

## Live Site

[https://rodionsteshenko.github.io/agent_chronicles/](https://rodionsteshenko.github.io/agent_chronicles/)

## How It Works

1. Cron job triggers scene generation
2. AI reads current story state (characters, plot, world)
3. Generates next scene with header image
4. Publishes to GitHub Pages
5. Updates story state for continuity

## Local Development

```bash
bundle install
bundle exec jekyll serve
```

## Structure

- `_posts/` - Scene markdown files
- `_data/story_state.yml` - Narrative state tracker
- `_layouts/` - Page templates
- `assets/images/` - Scene header images
- `scripts/` - Generation utilities

---

*The pen writes itself. The tale unfolds.*
