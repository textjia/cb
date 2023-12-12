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

{% assign externalLinksData = data.externalLinks.links %}

<h2>Mexican Recipes:</h2>
<ul>
  {% for link in externalLinksData %}
    {% if "mexican" in link.tags %}
      <li><a href="{{ link.url }}">{{ link.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

</body>
</html>