---
layout: layout.html
title: Dish Page
externalLinks: externalLinks.json
---
# RECIPES BY DISH #

### Salad ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key2 == "salad" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>

### Soups & Stews ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key2 == "soups-stews" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>


