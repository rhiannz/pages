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

<a href="https://www.google.com/" style="color: black; text-decoration: underline;text-decoration-style: dotted;">custom link</a>

[Click me](http://www.google.com){: .btn}

<a href="https://rhiannz.github.io//portfolio/portfolio-1/"><img src='/images/overdose_cover.png' alt="HTML tutorial" style="width:700px;height:auto;"></a><br/><br/>Short description of portfolio item number 1



{% for post in site.projects %}
  {% include archive-single.html %}
{% endfor %}
