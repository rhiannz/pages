---
layout: archive
title: "About"
permalink: /about_me/
author_profile: true
---

{% include base_path %}

<p style="font-size: 23px">
  I am actively looking for a full-time job in a data-oriented role. As a recent graduate of the UC Berkeley MA Statistics program, I am trained in modern statistical and machine learning methods and have an undergraduate background in mathematics. I also have experience with languages and software such as Python, R, and SQL. I look forward to any opportunities to grow and contribute to others! 
</p>

<hr/>

# Contact

Email: &nbsp; <span style = "font-family:'Courier New',monospace;">rhiannzhang@gmail.com</span>

<form>
  First name:<br>
  <input type="text" name="firstname"><br>
  Last name:<br>
  <input type="text" name="lastname">
  <input type="submit" value="Submit">
</form>


{% for post in site.about_me %}
  {% include archive-single.html %}
{% endfor %}
