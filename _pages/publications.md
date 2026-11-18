---
layout: page
permalink: /publications/
title: publications
description: Selected journal articles, conference papers, and ATLAS notes, organized by year.
years: [2026, 2025, 2024, 2023, 2022, 2021, 2019, 2017]
nav: true
nav_order: 1
---
I’ve selected papers and notes to which I made key contributions. For my full publication record, see [INSPIRE](https://inspirehep.net/authors/1605504).

<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
{% endfor %}

</div>
