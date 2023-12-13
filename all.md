---
layout: layout.html
title: All Page
externalLinks: externalLinks.json
---
# ALL VIEW #

<ul>
    {%- assign sortedLinks = externalLinks.links | sort: 'title' -%}
    {%- for link in sortedLinks -%}
        <li><a href="{{ link.url }}">{{ link.title }}</a></li>
    {%- endfor -%}
</ul>
