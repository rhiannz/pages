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
</form> 

<iframe name="hidden_iframe" id="hidden_iframe" style="display:none;" onload="if(submitted) {}"></iframe>

function ajaxpost () {
  // (A) GET FORM DATA
  var form = document.getElementById("gform");
  var data = new FormData(form);
 
  // (B) AJAX REQUEST
  // (B1) POST DATA TO SERVER, RETURN RESPONSE AS TEXT
  fetch("1c-server.html", { method:"POST", body:data })
  .then(res=>res.text())
 
  // (B2) SHOW MESSAGE ON SERVER RESPONSE
  .then((response) => {
    console.log(response);
    if (response == "OK") { alert("SUCCESSFUL!"); }
    else { alert("FAILURE!"); }
  })
 
  // (B3) OPTIONAL - HANDLE FETCH ERROR
  .catch((err) => { console.error(err); });
 
  // (C) PREVENT FORM SUBMIT
  return false;
}

{% for post in site.about_me %}
  {% include archive-single.html %}
{% endfor %}
