---
sitemap:
  priority: 1
---

# Resume

Hi, I'm a software developer based in Paris and I work at Jawg. I'm a DevOPS and back-end developer who love open-source.
I like to code in Java, Javascript ([Node.js](https://nodejs.org/en/)) and [Rust](https://www.rust-lang.org).
My favorite UI library is [RiotJS](https://riot.js.org/).

Here is a list of projects that I [maintain](#my-projects) and [contribute](#my-contributions).

{% for projects in site.data.projects %}

## {{ projects.type }}

<div class="columns is-multiline is-8">
{% for project in projects.projects %}
  <div class="column is-4">
  <div class="box">
<div class="title is-5">{{ project.name }}</div>

<p>{{ project.description }}</p>



<div class="columns is-mobile is-multiline">
  {% if project.github %}
  <div class="column is-narrow">
    <a href="{{project.github}}" class="button is-outlined is-primary" target="/blank">Github project</a>
  </div>
  {% endif %}
  {% if project.page %}
  <div class="column is-narrow">
    <a href="{{project.page}}" class="button is-outlined is-primary" target="/blank">Project Page</a>
  </div>
  {% endif %}
  {% if project.doc %}
  <div class="column is-narrow">
    <a href="{{project.doc}}" class="button is-outlined is-primary" target="/blank">Documentation</a>
  </div>
  {% endif %}
  {% if project.demo %}
  <div class="column is-narrow">
    <a href="{{project.demo}}" class="button is-outlined is-primary" target="/blank">Live Demo</a>
  </div>
  {% endif %}
  {% if project.link %}
  <div class="column is-narrow">
    <a href="{{project.link}}" class="button is-outlined is-primary" target="/blank">Link</a>
  </div>
  {% endif %}
</div>

{% if project.languages %}
<div class="languages-list">
{% for language in project.languages %}
<span class="dot dot-{{ language }}"></span>
<span class="language">{{ language }}</span>
{% endfor %}
</div>
{% endif %}
</div>
</div>
{% endfor %}
</div>

{% endfor %}
