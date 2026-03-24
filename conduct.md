---
layout: page
title: Code of conduct
description: How we show up for each other at Southwest Tech.
permalink: /conduct/
---

Southwest Tech is built on a simple idea — technology is for everyone, and everyone deserves to feel welcome at our meetups.

We call it the **"No Dicks" policy**. It's not a long legal document. It's just a shared understanding of how we treat each other.

## What we ask of everyone

{% for rule in site.data.conduct.rules %}
{% if rule.type == "do" %}
### {{ rule.title }}

{{ rule.description }}

{% endif %}
{% endfor %}

## What we won't tolerate

{% for rule in site.data.conduct.rules %}
{% if rule.type == "dont" %}
### {{ rule.title }}

{{ rule.description }}

{% endif %}
{% endfor %}
