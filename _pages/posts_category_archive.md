---
layout: archive
permalink: /posts-categories/
title: "Posts by Category"
author_profile: false
---

{% include base_path %}
{% include group-by-array collection=site.posts field="categories" %}


<ul class="taxonomy__index">
{% for category in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <li>
      <a href="#{{ category | slugify }}">
      <span>
        <i class="fas fa-link"></i>
        <strong>&nbsp;{{ category }}</strong>
      </span>
      <span>{{ group_items[forloop.index0].size }}</span>
      </a>
  </li>
{% endfor %}
</ul>



{% for category in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ category | slugify }}" class="archive__subtitle">{{ category }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
