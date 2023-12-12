---
title: Home Page
externalLinks: externalLinks.json
---

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>{{ title }}</title>
</head>
<body>
    # Welcome to My Site


    ### Turkish

    <ul>
        {% for link in externalLinks.links %}
            {% if "turkish" in link.categories %}
                <li><a href="{{ link.url }}">{{ link.title }}</a></li>
            {% endif %}
        {% endfor %}
    </ul>

    ### Mexican

    <ul>
        {% for link in externalLinks.links | where: "categories", "mescian" %}
            
                <li><a href="{{ link.url }}">{{ link.title }}</a></li>
            
        {% endfor %}
    </ul>



</body>
</html>