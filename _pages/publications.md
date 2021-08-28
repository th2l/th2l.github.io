---
layout: page
permalink: /publications/
title: publications
description:
nav: true
---

<div class="publications">

{% for y in (2016..2030) reversed %}
  {% capture count_conf %} {% bibliography_count -f papers --query @inproceedings[year = {{y}}] %} {% endcapture %}
  {% capture count_journal %} {% bibliography_count -f papers --query @article[year = {{y}}] %} {% endcapture %}
  {% assign count_papers = count_conf | plus: count_journal %}
  {% if count_papers > 0 %}
    <h2 class="year">{{y}}</h2>
    {% bibliography -f papers -q @*[year={{y}}]* %}
  {% endif %}
  {% endfor %}


</div>
