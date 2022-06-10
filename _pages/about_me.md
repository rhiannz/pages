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

<form name="gform" id="gform" enctype="text/plain" action="https://docs.google.com/forms/d/e/1FAIpQLSf2rcIOe5JCeeVmf0dyA5T5paxStMnz-KR8zEhDdn7kQveIUA/formResponse?usp=pp_url" target="hidden_iframe" onsubmit="setTimeout(function(){window.location.reload();},10);">
  Name: &nbsp; <input type="text" name="entry.1617483516" placeholder="Your Name" id="entry.1617483516"><br>
  Email: &emsp; <input type="text" name="entry.1417233657" id="entry.1417233657">
  Message:<br>
  <textarea name="entry.1487389352" id="entry.1487389352"></textarea>
  <input type="submit" value="Submit" style="color: teal">
</form> 

<iframe name="hidden_iframe" id="hidden_iframe" style="display:none;" onload="if(submitted) {}"></iframe>

{% for post in site.about_me %}
  {% include archive-single.html %}
{% endfor %}
