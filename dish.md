---
layout: layout.html
title: Dish Page
externalLinks: externalLinks.json
---
# RECIPES BY DISH #

{% assign totalCount = 0 %}

### Entree ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key2 == "entree" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
            {% assign totalCount = totalCount | plus: 1 %}
        {% endif %} 
    {% endfor %}
</ul>


### Veggie ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key2 == "veggie" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
            {% assign totalCount = totalCount | plus: 1 %}
        {% endif %} 
    {% endfor %}
</ul>

### Entree ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key2 == "entree" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
            {% assign totalCount = totalCount | plus: 1 %}
        {% endif %} 
    {% endfor %}
</ul>

### Noodle ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key2 == "noodle" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
            {% assign totalCount = totalCount | plus: 1 %}
        {% endif %} 
    {% endfor %}
</ul>

<p>Total # of recipes so far: {{ totalCount }}</p>

