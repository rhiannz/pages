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

<form name="gform" id="gform" enctype="text/plain" action="https://docs.google.com/forms/d/e/1FAIpQLSf2rcIOe5JCeeVmf0dyA5T5paxStMnz-KR8zEhDdn7kQveIUA/formResponse?usp=pp_url" target="hidden_iframe" onsubmit="submitted=true;">
  Name:<br>
  <input type="text" name="entry.1617483516" id="entry.1617483516"><br>
  Email:<br>
  <input type="text" name="entry.1417233657" id="entry.1417233657">
  Message:<br>
  <input type="text" name="entry.1487389352" id="entry.1487389352">
  <input type="submit" value="Submit">
    <script src="assets/js/jquery.min.js"></script>
    <script type="text/javascript">var submitted=false;</script>
    <script type="text/javascript">
    $('#gform').on('submit', function(e) {
      $('#gform *').fadeOut(2000);
      $('#gform').prepend('Your submission has been processed...');
      });
    </script>
</form> 

<iframe name="hidden_iframe" id="hidden_iframe" style="display:none;" onload="if(submitted) {}"></iframe>



{% for post in site.about_me %}
  {% include archive-single.html %}
{% endfor %}
