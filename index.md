---
title: Fire Learn
description: Learning site for FIRE!
layout: default
class: christchurch
layoutclass: default
---

---

## Get Started!
{% assign sorted_pages = site.pages | sort: 'url' | where: 'layout', 'lesson' %}
{% for sect in sorted_pages  %}
{% assign sect_parts_size =  sect.url | split: '/' | size %}
{% if sect_parts_size == 2 %}

* [{{sect.title}}]({{sect.url | relative_url}})
{% endif %}
{% endfor %} 

---
