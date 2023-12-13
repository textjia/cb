---
layout: layout.html
title: Country Page
externalLinks: externalLinks.json
---
# RECIPES BY COUNTRY #

### American ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key1 == "american" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>



