---
layout: page
permalink: /publications/
title: publications
description: (*) denotes equal contribution
years: [2026,2025,2024,2023,2022,2021,2020]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->

<div class="publications">


<h2>Accepted</h2>

{%- for y in page.years %}
   {% capture count %}{% bibliography_count -f papers -q @*[year={{y}} && keywords=accepted] %}{% endcapture %}
  {% assign count = count | plus: 0 %}

  {% if count > 0 %}
    <h2 class="year">{{y}}</h2>
    {% bibliography -f papers -q @*[year={{y}} && keywords=accepted] %}
  {% endif %}
{% endfor %}



<h2>Publications</h2>

{%- for y in page.years %}
   {% capture count %}{% bibliography_count -f papers -q @*[year={{y}} && keywords=publication] %}{% endcapture %}
  {% assign count = count | plus: 0 %}

  {% if count > 0 %}
    <h2 class="year">{{y}}</h2>
    {% bibliography -f papers -q @*[year={{y}} && keywords=publication] %}
  {% endif %}
{% endfor %}

<h2>Submitted</h2>


{%- for y in page.years %}
   {% capture count %}{% bibliography_count -f papers -q @*[year={{y}} && keywords=submitted] %}{% endcapture %}
  {% assign count = count | plus: 0 %}

  {% if count > 0 %}
    <h2 class="year">{{y}}</h2>
    {% bibliography -f papers -q @*[year={{y}} && keywords=submitted] %}
  {% endif %}
{% endfor %}
