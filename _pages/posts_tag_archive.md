---
layout: archive
permalink: /posts-tags/
title: "Posts by Tags"
author_profile: false
---

{% include base_path %}


{% include group-by-array collection=site.posts field="tags" %}
<ul class="taxonomy__index">
{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <li>
      <a href="#{{ tag }}">
      <span>
        <i class="fas fa-link"></i>
        <strong>&nbsp;{{ tag }}</strong>
      </span>
      <span>{{ group_items[forloop.index0].size }}</span>
      </a>
  </li>
{% endfor %}
</ul>

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}