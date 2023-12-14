---
layout: layout.html
title: Country Page
externalLinks: externalLinks.json
---
# RECIPES BY COUNTRY #

### Generic ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key1 == "generic" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>

### Russian ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key1 == "russian" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>

### Generic ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key1 == "chinese" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>



