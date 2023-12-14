---
layout: layout.html
title: Title Page
externalLinks: externalLinks.json
pagination:
  data: externalLinks.links
  size: 9
  alias: paginatedLinks
  reverse: false
---
# TITLE VIEW
<p id="totalCountPlaceholder"></p>
{% assign totalCount = 0 %}

        <ul class="list-group">
    {%- assign sortedPaginatedLinks = paginatedLinks | sort: 'title' -%}
    {%- for paginatedLink in sortedPaginatedLinks %}
        <li><a href="{{ paginatedLink.url }}">{{ paginatedLink.title }} - {{ paginatedLink.id }}</a></li>
        {% assign totalCount = totalCount | plus: 1 %}
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

        <p>Total # of recipes so far: {{ totalCount }}</p>

        <script>
  // Wait for the DOM to be ready
  document.addEventListener('DOMContentLoaded', function() {
    // Get the totalCount value
    var totalCountValue = {{ totalCount }};

    // Find the placeholder element
    var totalCountPlaceholder = document.getElementById('totalCountPlaceholder');

    // Move totalCount to the placeholder
    totalCountPlaceholder.textContent = 'Total # of recipes so far: ' + totalCountValue;
  });
</script>
