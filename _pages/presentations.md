---
layout: page
title: presentations
permalink: /presentations/
description: A gradual progression into improving my public speaking skills.
nav: true
---

{% for presentation in site.data.presentations %}
    {% if forloop.first == false %}
<hr/>
    {% endif %}

<h4>{{presentation.title}} - {{presentation.date}}</h4>
<h5>{{presentation.event}} | {{presentation.location}}</h5>

{% if presentation.url %}
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/{{presentation.url}}" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
{% endif %}
{% endfor %}

