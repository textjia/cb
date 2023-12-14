---
layout: layout.html
title: Ingredient Page
externalLinks: externalLinks.json
---
# RECIPES BY INGREDIENT #

### Beef ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key3 == "beef" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>

### Cauliflower ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key3 == "cauliflower" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>

### Shrimp ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key3 == "shrimp" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>





