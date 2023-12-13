---
layout: layout.html
title: Ingredient Page
externalLinks: externalLinks.json
---
# RECIPES BY INGREDIENT #

### Beef-Tripe ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key3 == "beef-tripe" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>

### Corn ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key3 == "corn" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>

### Eggplant ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key3 == "eggplant" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>


