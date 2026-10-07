---
layout: page
title: Events
description: Upcoming Southwest Tech meetups.
permalink: /events/
---

Southwest Tech is a new initiative and the first event is very much an experiment — we want to see if there's enough interest and demand to keep this going. The plan is to meet every six weeks, but how often we run events will depend on how things go.

If you're interested, RSVP and come along. That's the best signal we can get.

---

{% assign past = site.events | sort: 'date' | reverse | where_exp: "e", "e.date < site.time" %}

## Upcoming

{% include luma-calendar.html %}

{% if past.size > 0 %}
## Past events

{% for event in past %}
{% include event-card.html event=event %}
{% endfor %}
{% endif %}
