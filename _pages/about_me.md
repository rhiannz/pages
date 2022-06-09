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

<!DOCTYPE html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    <title>contact form</title>
</head>

<body>

<link href="contact-form.css" rel="stylesheet">

<div class="fcf-body">

    <div id="fcf-form">
    <h3 class="fcf-h3">Contact us</h3>

    <form id="fcf-form-id" class="fcf-form-class" method="post" action="contact-form-process.php">
        
        <div class="fcf-form-group">
            <label for="Name" class="fcf-label">Your name</label>
            <div class="fcf-input-group">
                <input type="text" id="Name" name="Name" class="fcf-form-control" required>
            </div>
        </div>

        <div class="fcf-form-group">
            <label for="Email" class="fcf-label">Your email address</label>
            <div class="fcf-input-group">
                <input type="email" id="Email" name="Email" class="fcf-form-control" required>
            </div>
        </div>

        <div class="fcf-form-group">
            <label for="Message" class="fcf-label">Your message</label>
            <div class="fcf-input-group">
                <textarea id="Message" name="Message" class="fcf-form-control" rows="6" maxlength="3000" required></textarea>
            </div>
        </div>

        <div class="fcf-form-group">
            <button type="submit" id="fcf-button" class="fcf-btn fcf-btn-primary fcf-btn-lg fcf-btn-block">Send Message</button>
        </div>

        <div class="fcf-credit" id="fcf-credit">
        Simple HTML email form provided by <a href="https://www.majesticform.com" target="_blank">MajesticForm</a>
        </div>

    </form>
    </div>

</div>

</body>
</html>



{% for post in site.about_me %}
  {% include archive-single.html %}
{% endfor %}
