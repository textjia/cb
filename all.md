---
layout: layout.html
title: Home Page
externalLinks: externalLinks.json
---
# ALL VIEW #

<ul>
    {%- for link in externalLinks.links | sortByName -%}
        
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        
    {%- endfor -%}
</ul>

