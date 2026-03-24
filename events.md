---
layout: page
title: Events
description: Upcoming Southwest Tech meetups.
permalink: /events/
---

{% assign upcoming = site.events | sort: 'date' | where_exp: "e", "e.date >= site.time" %}
{% assign past = site.events | sort: 'date' | reverse | where_exp: "e", "e.date < site.time" %}

{% if upcoming.size > 0 %}
## Upcoming

{% for event in upcoming %}
{% include event-card.html event=event %}
{% endfor %}

{% else %}
<div class="no-events">
  <p>No events scheduled yet. Check back soon, or <a href="/get-involved/">get involved</a> to help organise the first one.</p>
</div>
{% endif %}

{% if past.size > 0 %}
## Past events

{% for event in past %}
{% include event-card.html event=event %}
{% endfor %}
{% endif %}
