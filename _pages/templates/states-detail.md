---
layout: template
categories: [templates, states]
type: [detail-page]
title: States Detail Page
permalink: /templates/states/deail
overview: This template is used for finding information by state or territory.

description:  The States Landing template houses various resources and information by state.

prototype:
  - name: States Detail
    link: /prototype/states/detail

specs:
  - name: Title
    type: h1
    authored: no
    required: yes
    content: name of the state or territory
    searchable: yes
  - name: Summary
    type: usa-intro
    authored: yes
    required: yes
    content: 250 character max
    searchable: yes
  - name: FAQ Accordions
    subhead: yes
    type: accordion
  - name: Section title
    type: text
    authored: yes
    required: yes
    content: 80 character max
  - name: Inner Accordion
    subsubhead: yes
    type: accordion
    notes: CMS should use a list to create
  - name: Label
    type: accordion-label
    authored: yes
    required: yes
    content: 80 character max
  - name: Content
    type: accordion
    authored: yes
    required: yes
    content: allows h2, h3, h4, bullets, links, blockquotes

alert:
  content: Before developing page layout, please be sure to read about our <a class="usa-link" href="/styles/grids/">Grid System</a>
  type: warning
---

## Functionality Specifications

{% include patterns/alert/alert-no-icon-jk.md %}

### FAQ Accordions
- OnPageLoad the main accordion is closed
- onClick/onTap -- the accordion opens to show all the sub accordions (which are closed)
- The main accordion stays open until closed by the user
- onClick/onTap of the sub accordion -- opens to show content inside. 
- Only one sub accordion is open at a time

### Search
- Search is pre-filtered to the given state or territory. 
- The location filter is hidden

See more about [search](/templates/search) <i class="fa-kit fa-navigate-next"></i>