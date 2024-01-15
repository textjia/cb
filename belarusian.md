---
layout: layout.html
title:  Belarusian
externalLinks: externalLinks.json
---

<font face="Courier" size="1">[{{ title }}]</font>





       <table border="0">

     {%- assign sortedLinks = externalLinks.links | sort: 'title' -%}

     {% for link in sortedLinks %}
        {% if link.key1 == "belarusian" %}
            <tr><td><a href="{{ link.image }}" target="right-top" onClick="window.parent.frames['right-bottom'].location='{{ link.url}}';"><font face="Courier" size="1">{{ link.title }}</font></a></td></tr>

        {% endif %} 
    {% endfor %}

</table>