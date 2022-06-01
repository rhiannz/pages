---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

## title

blahblah

[an example site](https://rhiannz.github.io//portfolio/portfolio-1/)

<a href="https://www.google.com/" style="color: black; text-decoration: none;">custom link</a>

<a href="https://www.google.com/" style="font-size: 40px; color: black; text-decoration: none;">custom link</a>

[Click me](http://www.google.com){: .btn}

<a href="https://rhiannz.github.io//portfolio/portfolio-1/" style="color: blue; text-decoration: none; background-color:blue;" class="btn">See more</a>

<a href="https://rhiannz.github.io//portfolio/portfolio-1/" class="btn" style="color: black; text-decoration: none; background-color:CornflowerBlue;">See more</a>


<a href="https://rhiannz.github.io//portfolio/portfolio-1/"><img src='/images/overdose_cover.png' alt="HTML tutorial" style="width:700px;height:auto;"></a><br/><br/>Short description of portfolio item number 1

<a href="https://rhiannz.github.io//portfolio/portfolio-1/"><img src='/images/overdose_cover.png' alt="HTML tutorial" style="width:750px;height:auto;"></a><br/><br/>Short description of portfolio item number 1



{% for post in site.projects %}
  {% include archive-single.html %}
{% endfor %}
