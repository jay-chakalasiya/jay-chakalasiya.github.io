---
title: Projects
layout: collection
permalink: /projects/
collection: projects
---

{% include base_path %}

{% if paginator %}
  {% assign posts = paginator.projects %}
{% else %}
  {% assign posts = site.projects %}
{% endif %}

<div class="grid__wrapper">
  {% for project in projects %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>




{% include paginator.html %}
