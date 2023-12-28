---
layout: layout.html
title: Title Page
externalLinks: externalLinks.json
pagination:
  data: externalLinks.links |  sort: 'title' 
  size: 33
  alias: paginatedLinks
  reverse: false
---
<font face="Courier" size="1">by Recipe Title</font>

{% assign totalCount = 0 %}
{% assign sortedLinks = externalLinks.links | sort: 'title' %}

<table border="0">
  {%- for paginatedLink in paginatedLinks -%}
    <tr>
      <td>
        <a href="{{ paginatedLink.image }}" target="right-top" onClick="window.parent.frames['right-bottom'].location='{{ paginatedLink.url}}';">
          <font face="Courier" size="1">{{ paginatedLink.title }}</font>
        </a>
      </td>
    </tr>
    {% assign totalCount = totalCount | plus: 1 %}
  {%- endfor -%}
</table>



   <table border=0 cellpadding=3 width=32 height=32>
        <tr>
        
        {% if pagination.href.previous %}      
                <td><a class="page-link" href="{{ pagination.href.previous }}" tabindex="-1"><font face="Courier" size="1">Previous</font></a></td>     
        {% endif %}
        
        {% for pageNumber in pagination.pages %}
              <td><a class="page-link" href="{{ pagination.hrefs[forloop.index0] }}"><font face="Courier" size="1">{{ forloop.index }}</font></a></td>
        {% endfor %}
        
        {% if pagination.href.next %}
              <td>
                <a class="page-link" href="{{ pagination.href.next }}"><font face="Courier" size="1">Next</font></a>
              </td>
        {% endif %}
        
        </tr>
        </table>

        

