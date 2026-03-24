# Southwest Tech

Website for the Southwest Tech community — technology enthusiasts in the Dunsborough, Busselton, and Margaret River region of Western Australia.

Built with [Jekyll](https://jekyllrb.com/) and hosted on GitHub Pages.

## Local development

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000

## Adding an event

Create a new file in `_events/` following this naming convention:

```
_events/YYYY-MM-DD-event-name.md
```

Use this front matter template:

```yaml
---
layout: event
title: "Southwest Tech #2 — Monthly meetup"
date: 2026-06-18
time: "6:00pm – 8:30pm"
location: Venue Name, Town
excerpt: A one-line description for the events listing.
rsvp_url: https://...
---

Event description goes here.
```

## Structure

```
_data/          # Site data (topics, nav, conduct)
_events/        # Event posts
_includes/      # Header, footer, partials
_layouts/       # Page templates
assets/         # CSS, JS, images
*.md / *.html   # Pages (index, about, events, conduct, get-involved)
```

## Deployment

Pushes to `main` automatically deploy via GitHub Actions to GitHub Pages.
