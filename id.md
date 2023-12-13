---
layout: layout.html
title: Home Page
externalLinks: externalLinks.json
---
# ID VIEW


<ul>
    {% for link in externalLinks.links %}
       
            <li><a href="{{ link.url }}">{{ link.id }} - {{ link.title }}</a></li>
         
    {% endfor %}
</ul>

