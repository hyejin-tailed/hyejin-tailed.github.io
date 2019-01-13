---
layout: archive
permalink: /memory-leaks/
title : "Memory Leaks"
author_profile: true
header:
  image: "_pages/images/1.0.jpg"
---

See? It was just simple segue between profile tab in main.async thread using Grand Central Dispatch.

{% include base_path %}
{% include group-by-array collection=site.post field="tags" %}

{% for tag in group names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }} class="archive_subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor%}