---
title: "Blog"
layout: splash
permalink: /blog/
header:
  overlay_image: "images/features/coffee-with-notepad.jpg"
  overlay_color: "#333"
  overlay_filter: 0.5
---

{% include base_path %}

{% for post in site.posts %}
  {% include archive-single.html %}
{% endfor %}