---
layout: layout.html
title: Home Page
externalLinks: externalLinks.json
pagination:
  data: collections.externalLinks
  size: 5               # Number of items per page
  alias: links        # Name for the pagination object in templates
  reverse: false          # Reverse the order (from Z to A)
  sort:
    attribute: title     # Sort based on the 'title' attribute
    type: string         # Specify the data type (in this case, string for alphabetical order)
---
# ALL VIEW #

<ul>
    {% for link in externalLinks.links | sort: 'data.externalLinks.title' %}
        
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        
    {% endfor %}
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

