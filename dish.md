---
layout: layout.html
title: Dish Page
externalLinks: externalLinks.json
---
# RECIPES BY DISH #

### Veggie ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key2 == "veggie" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>



