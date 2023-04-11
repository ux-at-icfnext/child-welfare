---
layout: default
# categories: [prototype]
title: Prototype Page
type: [prototype]
permalink: /prototype/
---
<div class="grid-container" markdown="1">
## Home Page (*Draft*)
<a href="/prototype/home">Home</a>

## Basic Pages
{% for basic in site.data.contentful.spaces.example.basic %}
  <a href="/prototype/{{basic.slug}}">{{basic.title}}</a>
{%endfor%}

## Resource Details (*Draft*)
{% for resources in site.data.contentful.spaces.example.resource %}
  <a href="/prototype/{{resources.slug}}">{{resources.title}}</a>
{%endfor%}

## Overview
{% for resources in site.data.contentful.spaces.example.topic %}
  <a href="/prototype/{{resources.slug}}">{{resources.title}}</a>
{%endfor%}

## Topic & Subtopics (*Draft*)
{% for resources in site.data.contentful.spaces.example.subTopics %}
  <a href="/prototype/{{resources.slug}}">{{resources.title}}</a>
{%endfor%}

## Events (*Draft*)
<a href="/prototype/events/landing">Events Landing</a>
{% for resources in site.data.contentful.spaces.example.events %}
  <a href="/prototype/{{resources.slug}}">{{resources.title}}</a>
{%endfor%}

## State
<p><a href="/prototype/states/landing">State Landing</a></p>
<p><a href="/prototype/states/detail">State Detail</a></p>


## Campaign (*Draft*)
<p><a href="/prototype/campaign/1">Campaign Example 1</a></p>
<p><a href="/prototype/campaign/2">Campaign Example 2</a></p>

## Glossary
<a href="/prototype/glossary">Glossary</a>

## Search Pages (*Draft*)
<p><a href="/prototype/search">Global Search</a></p>
<p><a href="/prototype/search/events">Events Search</a></p>
<p><a href="/prototype/search/directory">Directory Search</a></p>
<p><a href="/prototype/search/resources">All Resources</a></p>

</div>




