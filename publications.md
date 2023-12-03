---
title: Publications
layout: page
description: Publications
permalink: "/publications/"
---

# Journal
{% bibliography --file papers -q @article %}

# Conference proceedings
{% bibliography --file papers -q @inproceedings %}



{% comment %}
{% assign curYear = 'now' | date: "%Y" | plus:0  %}
{% assign Years = (2013..curYear) %}

### Journal
{% for year in Years reversed %}
#### {{ year }}
{% bibliography --file papers -q @article[year={{ year }}] %}
{% endfor %}

### Conference proceedings
{% for year in Years reversed %}
#### {{ year }}
{% bibliography --file papers -q @inproceedings[year={{ year }}] %}
{% endfor %}
{% endcomment %}
