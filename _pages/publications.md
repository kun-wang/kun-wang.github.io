---
layout: publication
permalink: /publications/
title: publications
category: publication
years: [2020, 2019, 2018, 2017, 2016]
---

A list of my publications is available on [Google scholar](https://scholar.google.com/citations?user=9pDyyUAAAAAJ). 
My publications can also be found on the [arXiv](https://arxiv.org/search/advanced?advanced=1&terms-0-operator=AND&terms-0-term=%22Kun+Wang%22&terms-0-field=author&classification-physics=y&classification-physics_archives=quant-ph&classification-include_cross_list=include).


{% for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f kun-wang-publications -q @*[year={{y}}]* %}
{% endfor %}
