---
layout: single
author_profile: true
toc: true
permalink: /posts/
title: "Posts"
excerpt: "Minimal Mistakes is a flexible two-column Jekyll theme."

---


{% include base_path %}

<div class="grid__wrapper">
  {% for post in site.portfolio %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>