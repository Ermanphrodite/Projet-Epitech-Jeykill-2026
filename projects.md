---
layout: page
title: Projets
permalink: /projects/
order: 3
---

---
{: style="margin-bottom: 0px" :}

{% assign sorted_projects = site.projects | sort: 'date' | reverse %}

{% for project in sorted_projects %}

## [{{ project.title }}]({{ project.url | relative_url}})

{% assign img_name = project.title | slugify %}
[<img src="{{ '/assets/images/' | append: img_name | append: '.jpg' | relative_url }}" alt="{{ project.title }}" title="{{ project.title }}" style="width: 90%; height: 150px; object-fit: cover; display: block; margin: 10px auto; border-radius: 8px; border: 1px solid grey;">]({{ project.url | relative_url }})

{{ project.description }}

*Technologies utilisées : {{ project.technos | join: ', ' }}*

---

{% endfor %}