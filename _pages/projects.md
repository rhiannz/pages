---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

## title 

blahblah

# [an example site](https://rhiannz.github.io//portfolio/portfolio-1/)

<a href=https://rhiannz.github.io//portfolio/portfolio-1/ class=btn>"Geospatial Explanatory Modeling of the U.S. Drug Overdose Epidemic"</a>

[Click me](http://www.google.com){: .btn}

<a href="https://rhiannz.github.io//portfolio/portfolio-1/"><img src='/images/overdose_cover.png' alt="HTML tutorial" style="width:500px;height:auto;"></a><br/><br/>Short description of portfolio item number 1

{% for post in site.projects %}
  {% include archive-single.html %}
{% endfor %}
