---
layout: layout.html
title: Home Page
externalLinks: externalLinks.json
---
# CatJohn's GF Cookbook #
<p id="totalCountPlaceholder"></p>

{% assign totalCount = 0 %}

### Generic ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key1 == "generic" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
            {% assign totalCount = totalCount | plus: 1 %}
        {% endif %} 
    {% endfor %}
</ul>

### Russian ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key1 == "russian" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
            {% assign totalCount = totalCount | plus: 1 %}
        {% endif %} 
    {% endfor %}
</ul>

### Chinese ###

<ul>
    {% for link in externalLinks.links %}
        {% if link.key2 == "chinese" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
            {% assign totalCount = totalCount | plus: 1 %}
        {% endif %} 
    {% endfor %}
</ul>


<table border="0" cellpadding="3">
<tr>
<td><a class="page-link" href="/country/">COUNTRY</a></td>
<td><a class="page-link" href="/dish/">DISH</a></td>
<td><a class="page-link" href="/ingredient/">INGREDIENT</a></td>
<td><a class="page-link" href="/id/">ID</a></td>
<td><a class="page-link" href="/title/">TITLE</a></td>
<td><a class="page-link" href="/p32/">32</a></td>
<td><a class="page-link" href="/p64/">64</a></td>
<td><a class="page-link" href="/p128/">128</a></td>
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
    

 



