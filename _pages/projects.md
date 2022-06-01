---
layout: archive
title: "--Projects--"
permalink: /projects/
author_profile: true
---

{% include base_path %}

<a href="https://rhiannz.github.io//portfolio/portfolio-1/" style="font-size: 30px; color: black; text-decoration: none;">Geospatial Explanatory Modeling of the U.S. Drug Overdose Epidemic</a>

<a href="https://rhiannz.github.io//portfolio/portfolio-1/"><img src='/images/overdose_cover.png' alt="HTML tutorial" style="width:700px;height:auto;"></a>

Short description of portfolio item number 1

<a href="https://rhiannz.github.io//portfolio/portfolio-1/" style="text-decoration: none; background-color:cornflowerblue;" class="btn">See more</a>



<a href="https://rhiannz.github.io//portfolio/portfolio-2/" style="font-size: 20px; color: black; text-decoration: none;">An Analysis of AP Exam Participation Rates</a>

<a href="https://rhiannz.github.io//portfolio/portfolio-2/"><img src='/images/ap_cover.png' alt="HTML tutorial" style="width:700px;height:auto;"></a>

Short description of portfolio item number 2

<a href="https://rhiannz.github.io//portfolio/portfolio-2/" style="text-decoration: none; background-color:cornflowerblue;" class="btn">See more</a>



<a href="https://rhiannz.github.io//portfolio/portfolio-3/" style="font-size: 10px; color: black; text-decoration: none;">Replication of “Piso Firme” Program Impact Investigation</a>

<a href="https://rhiannz.github.io//portfolio/portfolio-3/"><img src='/images/hhh_cover.png' alt="HTML tutorial" style="width:700px;height:auto;"></a>

Short description of portfolio item number 3

<a href="https://rhiannz.github.io//portfolio/portfolio-3/" style="text-decoration: none; background-color:cornflowerblue;" class="btn">See more</a>




<a href="https://rhiannz.github.io//portfolio/portfolio-4/" style="font-size: 40px; color: black; text-decoration: none;">genetic-selectR Package Development</a>

<a href="https://rhiannz.github.io//portfolio/portfolio-4/"><img src='/images/ga_cover.png' alt="HTML tutorial" style="width:700px;height:auto;"></a>

Short description of portfolio item number 4

<a href="https://rhiannz.github.io//portfolio/portfolio-4/" style="text-decoration: none; background-color:cornflowerblue;" class="btn">See more</a>





<a href="https://www.google.com/" style="color: black; text-decoration: none;">custom link</a>


<a href="https://rhiannz.github.io//portfolio/portfolio-1/" style="text-decoration: none; background-color:cornflowerblue;" class="btn">See more</a>



{% for post in site.projects %}
  {% include archive-single.html %}
{% endfor %}
