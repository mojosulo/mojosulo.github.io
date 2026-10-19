---
layout: default
title: My Plotly Plots
permalink: /plots/
---

# Plotly Plots from Pre-Publication

{% assign images = site.static_files | where_exp: "item", "item.path contains '/assets/images/'" | where_exp: "item", "item.extname == '.png' or item.extname == '.PNG'" %}

{% for image in images %}
  <div style="display: inline-block; margin: 10px;">
    <a href="{{ image.path }}" target="_blank">
      <img src="{{ image.path }}" alt="Image" style="max-width: 1200px; border: 1px solid #ccc;">
    </a>
  </div>
{% endfor %}
