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

Upcoming events live on the [Southwest Tech Lu.ma calendar](https://luma.com/SouthwestTech) — create them there and they appear on the Events page automatically via the embed (`_includes/luma-calendar.html`). The calendar ID is set under `luma:` in `_config.yml`.

After a meetup, optionally add it to the archive in `_events/` so it shows under "Past events":

```
_events/YYYY-MM-DD-event-name.md
```

```yaml
---
layout: event
title: "Southwest Tech — October Meetup"
date: 2026-10-03
time: "2:00pm"
location: Venue Name, Town
excerpt: A one-line description for the events listing.
rsvp_url: https://luma.com/...
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

Pushes to `master` automatically deploy via GitHub Actions to GitHub Pages.
