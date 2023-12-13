---
layout: layout.html
title: Home Page
externalLinks: externalLinks.json
---
# CatJohn's GF Cookbook #

### Turkish ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key1 == "turkish" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>

### Mexican ###
<ul>
    {% for link in externalLinks.links %}
        {% if link.key1 == "mexican" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
        {% endif %} 
    {% endfor %}
</ul>

### Soup & Stews ###

<ul>
    {% for link in externalLinks.links %}
        {% if link.key2 == "soups-stews" %}
            <li><a href="{{ link.url }}">{{ link.title }}</a></li>
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

    

 



