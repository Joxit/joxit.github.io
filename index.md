---
title: Projects
---

{% for projects in site.data.projects %}

## {{ projects.type }}

{% for project in projects.projects %}

### {{ project.name }}

{{ project.description }}

{% if project.github %}[Github project](<{{ project.github }}>){: class="btn btn-primary" target="\_blank"}{% endif %} {% if project.page %}[Project Page]({{project.page}}){: class="btn btn-primary" target="\_blank"}{% endif %} {% if project.doc %}[Documentation]({{project.doc}}){: class="btn btn-primary" target="\_blank"}{% endif %} {% if project.demo %}[Live Demo](<{{ project.demo }}>){: class="btn btn-primary" target="\_blank"}{% endif %}

{% endfor %}

{% endfor %}
