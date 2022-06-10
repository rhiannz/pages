---
layout: archive
title: "About"
permalink: /about_me/
author_profile: true
---

{% include base_path %}

# Contact

<form name="gform" id="gform" enctype="text/plain" action="https://docs.google.com/forms/d/e/1FAIpQLSf2rcIOe5JCeeVmf0dyA5T5paxStMnz-KR8zEhDdn7kQveIUA/formResponse?usp=pp_url" target="hidden_iframe" onsubmit="setTimeout(function(){window.location.reload();},10);">
  <input type="text" name="entry.1617483516" placeholder="Your name" id="entry.1617483516"><br>
  <input type="text" name="entry.1417233657" placeholder="Your email" id="entry.1417233657" >
  <textarea name="entry.1487389352" placeholder="Type your message here" id="entry.1487389352" rows="10" ></textarea>
  <input type="submit" value="Submit" style="color: white; background-color: cornflowerblue">
</form> 

<iframe name="hidden_iframe" id="hidden_iframe" style="display:none;" onload="if(submitted) {}"></iframe>


Email: &nbsp; <span style = "font-family:'Courier New',monospace;">rhiannzhang@gmail.com</span>


{% for post in site.about_me %}
  {% include archive-single.html %}
{% endfor %}
