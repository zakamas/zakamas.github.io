---
layout: page
permalink: /publications/
title: publications
description: Publications are listed in reversed chronological order. 
years: [2020, 2017, 2015]
# refs: [samak,kirci2015healthcare]
---

{% for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

<!-- {% for r in page.refs %}
  {% bibliography -f papers -q @*[key = {{r}}] %}
{% endfor %} -->
