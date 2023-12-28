---
layout: layout.html
title:  Recent Adds
externalLinks: externalLinks.json
---

<font face="Courier" size="1">[{{ title }}]</font>





       <table border="0">

     {%- assign sortedLinks = externalLinks.links | sort: 'date' | reverse -%}

     {% for link in sortedLinks %}
        
            <tr><td><a href="{{ link.image }}" target="right-top" onClick="window.parent.frames['right-bottom'].location='{{ link.url}}';"><font face="Courier" size="1">{{ link.date | date: "%m/%d/%y"}} - {{ link.title }}</font></a></td></tr>

        
    {% endfor %}

</table>