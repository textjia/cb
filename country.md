---
layout: layout.html
title: Country Page
externalLinks: externalLinks.json
---
# RECIPES BY COUNTRY #

### Mexican ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key1 == "mexican" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>

### Turkish ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key1 == "turkish" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>

