---
layout: page
permalink: /publications/
title: Publications
description: 
years: [2023, 2022, 2020]
nav: true
nav_order: 1
---

Most updated publications on [google scholar](https://scholar.google.com/citations?user=gf-2IBkAAAAJ). 

<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
