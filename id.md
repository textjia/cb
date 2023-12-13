---
layout: layout.html
title: ID Page
externalLinks: externalLinks.json
pagination:
  data: externalLinks.links
  size: 9
  alias: paginatedLinks
  reverse: false
---
# ID VIEW


        <ul class="list-group">
    {%- assign sortedPaginatedLinks = paginatedLinks | sort: 'id' -%}
    {%- for paginatedLink in sortedPaginatedLinks %}
        <li><a href="{{ paginatedLink.url }}">{{ paginatedLink.id }} - {{ paginatedLink.title }}</a></li>
    {%- endfor %}
</ul>

   <table border=0 cellpadding=3 width=32 height=32>
        <tr>
        
        {% if pagination.href.previous %}      
                <td><a class="page-link" href="{{ pagination.href.previous }}" tabindex="-1">Previous</a></td>     
        {% endif %}
        
        {% for pageNumber in pagination.pages %}
              <td><a class="page-link" href="{{ pagination.hrefs[forloop.index0] }}">{{ forloop.index }}</a></td>
        {% endfor %}
        
        {% if pagination.href.next %}
              <td>
                <a class="page-link" href="{{ pagination.href.next }}">Next</a>
              </td>
        {% endif %}
        
        </tr>
        </table>
