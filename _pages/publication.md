---
layout: page
permalink: /publication/
title: publication
description:
nav: true
page_order: 2
---

<div class="publications">

{% for y in (2016..2030) reversed %}
  {% capture count_conf %} {% bibliography_count -f papers --query @inproceedings[year = {{y}}] %} {% endcapture %}
  {% capture count_journal %} {% bibliography_count -f papers --query @article[year = {{y}}] %} {% endcapture %}
  {% assign count_papers = count_conf | plus: count_journal %}
  {% if count_papers > 0 %}
    {% bibliography -f papers -q @*[year={{y}}]* %}
  {% endif %}
  {% endfor %}


</div>
