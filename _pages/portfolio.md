---
layout: splash
title: "Project Portfolio"
permalink: /portfolio/
author_profile: false
header:
  overlay_image: /images/features/space.jpg
  caption: "The Horsehead Nebula"
---

{% include base_path %}

<div class="grid__wrapper">
  {% for post in site.portfolio %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>