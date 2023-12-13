---
layout: layout.html
title: Home Page
externalLinks: externalLinks.json
---
# CatJohn's GF Cookbook #

### Turkish ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key1 == "turkish" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>

### Mexican ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key1 == "mexican" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>

### Soup & Stews ###

<ul>
    {% for link in externalLinks.links %}
        {% if link.key2 == "soups-stews" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>

    

 



