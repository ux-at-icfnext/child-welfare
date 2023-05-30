---
layout: template
categories: [templates, states]
type: [detail-page]
title: States Landing Page
permalink: /templates/states/landing
overview: This template is used for finding information by state or territory.

description:  The States Landing template houses various resources and information by state.


specs:
  - name: Title
    type: h1
    authored: no
    required: yes
    content: "Find information by State"
    searchable: yes
  - name: Summary
    type: usa-intro
    authored: yes
    required: yes
    content: 250 character max
    searchable: yes
  - name: hex map label
    type: text
    authored: no
    required: yes
    content: "Choose your state or territory below"
  - name: hex map
    type: interactive -- see below

prototype:
  - name: States Landing
    link: /prototype/states/landing

alert:
  content: Before developing page layout, please be sure to read about our <a class="usa-link" href="/styles/grids/">Grid System</a>
  type: warning
---
## Functionality Specifications

{% include patterns/alert/alert-no-icon-jk.md %}

## Select Menus
OnPage load on the the first menu shows
- -- Select Area --
- States
- Territories 
- Tribes

OnSelect the second menu appears with the options related to the above. _(See content team for list of tribes)_

## Map
_The prototype uses an image a representative of this experience_
- onHover/onHold - the state grows and changes color
- onClick/onTap - the system goes to the appropriate linked page.
