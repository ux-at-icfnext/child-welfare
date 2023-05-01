---
layout: template
categories: [templates]
type: [sub-nav-item]
title: Campaign Page
permalink: /templates/campaign
overview: This template is used for campaigns and initiatives.

description: This template is used for campaigns and initiatives. The author has flexibility over the look and feel by choosing different content objects. The prototype shows two possible layouts.

prototype:
  - name: Campaign Example 1
    link: /prototype/campaign/1
  - name: Campaign Example 2
    link: /prototype/campaign/2

alert:
  content: Before developing page layout, please be sure to read about our <a class="usa-link" href="/styles/grids/">Grid System</a>
  type: warning

heros:
  - name: Hero option
    type: hero
    authored: yes
    required: yes
    content: " campaign page hero - choose between: blue, gray or white backround"
    searchable:
    source:
    notes:
  - name: Title
    type: h1
    authored: yes
    required: yes
    content: 80 characters max
    searchable: yes
  - name: Summary
    type: usa-intro
    authored: yes
    required: yes
    content: 250 characters max
    searchable: yes
  - name: Button label
    type: button
    authored: yes
    required: yes
    content: 80 characters max
  - name: Button Link
    type: url
    authored: yes
    required: yes

impact1:
  - name: Title
    type: h1
    authored: yes
    required: yes
    content: 80 characters max
    searchable: yes
  - name: Summary
    type: usa-intro
    authored: yes
    required: yes
    content: 250 characters max
    searchable: yes
  - name: pie chart
    type: infographic
    authored: yes
    required: yes
impact2:
  - name: Title
    type: h1
    authored: yes
    required: yes
    content: 80 characters max
    searchable: yes
  - name: Summary
    type: usa-intro
    authored: yes
    required: yes
    content: 250 characters max
    searchable: yes
  - name: Stats List
    subhead: yes
    type: list
    authored: yes
    required: yes
    content: limit 4
  - name: Stats
    type: number
    authored: yes
    required: yes
  - name: Description
    type: text
    authored: yes
    required: yes
    content: 140 characters max
  
vision:
  - name: Content
    type: text
    authored: yes
    required: yes
    content: 250 characters max

involved:
  - name: Title
    type: h3
    authored: yes
    required: yes
    content: 80 characters max
  - name: Content
    type: text
    authored: yes
    required: yes
    content: 250 characters max
  - name: Button label
    type: button
    authored: yes
    required: yes
    content: 80 characters max
  - name: Button Link
    type: url
    authored: yes
    required: yes
---
# SPECS STILL IN PROGRESS!!

## Layout Specifications

{% include patterns/alert/alert-no-icon-jk.md %}

### Page order
The hero needs to be at the top of the page, outside of that, the author should be able to pick the order. This rest the page highlights the content blocks.

### Hero
Authors can choose between the different hero backgrounds (blue, gray and white)
{% include partials/content-specs.md content=page.heros %}

### Vision Statement
{% include partials/content-specs.md content=page.vision %}

### Our Impact (with pie chart)
{% include partials/content-specs.md content=page.impact1 %}

### Our Impact (with stats)
{% include partials/content-specs.md content=page.impact2 %}

### Get Involved
{% include partials/content-specs.md content=page.involved %}