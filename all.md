---
layout: layout.html
title: Home Page
externalLinks: externalLinks.json
---
# ALL VIEW #

<ul>
    {%- assign sortedLinks = externalLinks.links | sort: 'title' -%}
    {%- for link in sortedLinks -%}
        <li><a href="{{ link.url }}">{{ link.title }}</a></li>
    {%- endfor -%}
</ul>
