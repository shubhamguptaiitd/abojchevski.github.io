---
layout: page
permalink: /publications/
title: Publications
description: publications in reversed chronological order </br> * denotes equal contribution # by categories </br>
years: [2021, 2020, 2019, 2018, 2017]
nav: true
sort: 3
---

<div class="publications">
<!-- * denotes equal contribution -->
<!-- <h1> preprints </h1> -->

<p>An up-to-date list is available on <a href="https://scholar.google.com/citations?user=F1APiN4AAAAJ" target="_blank">Google Scholar</a>.</p>

<h1> conferences & journals </h1>
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}},category=conference]* %}
{% endfor %}

<h1> workshops </h1>
{% bibliography -f papers -q @*[category=workshop]* %}

<h1> theses </h1>
{% bibliography -f papers -q @*[category=thesis]* %}

</div>
