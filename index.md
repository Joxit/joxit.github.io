# Resume

Hi, I'm a software developer based in Paris and I work at Jawg. I'm a DevOPS and back-end developer who love open-source.
I like to code in Java, Javascript ([Node.js](https://nodejs.org/en/)) and [Rust](https://www.rust-lang.org).
My favorite UI library is [RiotJS](https://riot.js.org/).

Here is a list of projects that I [maintain](#my-projects) and [contribute](#my-contributions).

{% for projects in site.data.projects %}

## {{ projects.type }}

{% for project in projects.projects %}

### {{ project.name }}

{{ project.description }}

{% if project.github %}[Github project](<{{ project.github }}>){: class="btn btn-primary" target="\_blank"}{% endif %} {% if project.page %}[Project Page]({{project.page}}){: class="btn btn-primary" target="\_blank"}{% endif %} {% if project.doc %}[Documentation]({{project.doc}}){: class="btn btn-primary" target="\_blank"}{% endif %} {% if project.demo %}[Live Demo](<{{ project.demo }}>){: class="btn btn-primary" target="\_blank"}{% endif %}
{% if project.languages %}

<div class="languages-list">
{% for language in project.languages %}
<span class="dot dot-{{ language }}"></span>
<span class="language">{{ language }}</span>
{% endfor %}
</div>
{% endif %}
{% endfor %}

{% endfor %}
