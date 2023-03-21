---
layout: default
# categories: [prototype]
title: Prototype Page
type: [prototype]
permalink: /prototype/
---
<div class="grid-container" markdown="1">
## Basic Pages
{% for basic in site.data.contentful.spaces.example.basic %}
  <a href="/prototype/{{basic.slug}}">{{basic.title}}</a>
{%endfor%}

## Resource Details
{% for resources in site.data.contentful.spaces.example.resource %}
  <a href="/prototype/{{resources.slug}}">{{resources.title}}</a>
{%endfor%}

</div>

