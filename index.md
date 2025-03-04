---
title: Jones Magloire @Joxit
sitemap:
  priority: 1
---

# Resume

Hi, my name is Jones, I'm a **software engineer** and **photography enthusiast**.

As a **software engineer**, I'm the CTO of [Jawg](https://jawg.io) with main topics in R&D, DevOPS and back-end development with a specialization in *Geographic Information Systems*.
I'm also **a teacher at university** since 2017 where I teach final year master's students in computer science at the [Institut Galilée](https://galilee.univ-paris13.fr/). The [courses](https://joxit.dev/IG-Master2/) focus on technologies used in business such as JEE, Spring, Hibernate, Kotlin, React, VueJS... But also on cartography and OpenStreetMap since this is my specialization.
My favorite languages are Java/[Kotlin](https://kotlinlang.org/), Javascript ([Node.js](https://nodejs.org/en/)) and [Rust](https://www.rust-lang.org). I have some knowledges in front-end development, but that's not what I'm aiming for. But when I need it, I use [RiotJS](https://riot.js.org/) and [React](https://react.dev/) for my interfaces.

As a **photography enthusiast**, I take photos during my trips and post them on my [Instagram](https://www.instagram.com/jox.it/). I'm using a *Nikon D5200* with a *18-300mm F3.5-5.6* and *50mm F1.4* lenses and I like nature, architecture and street photography.

Here is a list of projects that I [created](#my-projects) and where I [contribute](#my-contributions).

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
