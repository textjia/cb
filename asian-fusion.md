---
layout: layout.html
title: Asian Fusion Page
externalLinks: externalLinks.json
---

<font face="Courier" size="1">[Asian Fusion]</font>





       <table border="0">
      
       {%- assign sortedLinks = externalLinks.links | sort: 'title' -%}

     {% for link in sortedLinks %}
        {% if link.key1 == "asian-fusion" %}
           <tr><td><a href="{{ paginatedLink.image }}" target="right-top" onClick="window.parent.frames['right-bottom'].location='{{ paginatedLink.url}}';"><font face="Courier" size="1">{{ paginatedLink.title }}</font></a></td></tr>
            
        {% endif %} 
    {% endfor %}

</table>



 






   




