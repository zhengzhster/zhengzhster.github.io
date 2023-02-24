---
layout: page
permalink: /publications/
title: publications
description: Select Publications(Publications Link to Google Scholar[https://scholar.google.com/citations?hl=en&user=siE8wmkAAAAJ&view_op=list_works&sortby=pubdate])
years: [2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014]
nav: true
nav_order: 2
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
