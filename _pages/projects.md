---
title: Projects
layout: collection
permalink: /projects/
collection: projects
entries_layout: grid
classes: wide
---


{% include base_path %}

<div class="grid__wrapper">
  {% for post in site.portfolio %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>