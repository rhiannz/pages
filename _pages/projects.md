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


[an example site](https://rhiannz.github.io//portfolio/portfolio-1/){
  color: blue;
  text-decoration: none; /* no underline */
}

[an example site](https://rhiannz.github.io//portfolio/portfolio-1/){
  border: none !important;
 }

<a href="https://www.google.com/" style="color: black; text-decoration: none;">custom link</a>

<a href="https://www.google.com/" style="font-size: 40px; color: black; text-decoration: none;">custom link</a>

[Click me](http://www.google.com){: .btn}

<a href="https://rhiannz.github.io//portfolio/portfolio-1/" style="font-size: 60px; color: black; text-decoration: none;" class="btn">"Geospatial Explanatory Modeling of the U.S. Drug Overdose Epidemic"</a>

<a href="https://rhiannz.github.io//portfolio/portfolio-1/" class="btn" style="font-size: 50px; color: black; text-decoration: none;">"Geospatial Explanatory Modeling of the U.S. Drug Overdose Epidemic"</a>


<a href="https://rhiannz.github.io//portfolio/portfolio-1/"><img src='/images/overdose_cover.png' alt="HTML tutorial" style="width:700px;height:auto;"></a><br/><br/>Short description of portfolio item number 1

<a href="https://rhiannz.github.io//portfolio/portfolio-1/"><img src='/images/overdose_cover.png' alt="HTML tutorial" style="width:800px;height:auto;"></a><br/><br/>Short description of portfolio item number 1



{% for post in site.projects %}
  {% include archive-single.html %}
{% endfor %}
