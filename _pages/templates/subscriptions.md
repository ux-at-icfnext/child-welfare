---
layout: template
categories: [templates]
type: [sub-nav-item]
title: Subscriptions 
permalink: /templates/subscriptions/
overview: The special page is used for showing available subscriptions.

description: |
    This special pages is used for showing available subscriptions.

prototype:
  - name: Subscriptions
    link: https://www.sketch.com/s/dd2f2e71-977c-45b4-baf3-8bf823bfcd0d/a/dlpjA5m

specs:
  - name: Title
    type: h1
    authored: yes
    required: yes
    content: 80 characters max
    searchable: yes
    source:
    notes: 
  - name: Summary
    type: text (usa-intro)
    authored: yes
    required: yes
    content: 250 characters max
    searchable: yes
  - name: Subtitle
    type: h2
    authored: no | static on template
    content: Learn more about our offerings
    notes: "front-end only"
  - name: Subscribe CTA
    type: uses subscribe pattern
    authored: "no"
    notes: front-end only
  - name: Section 
    type: multi-valued
    authored: yes
    content: See below

specs2:
  - name: Section Title
    type: h3
    authored: yes
    required: yes
    content: 80 characters max
  - name: Section summary
    type: text
    authored: yes
    required: yes
    content: 250 max characters
  - name: List
    type: usa-card
    authored: yes
    content: multi-valued table see below

specs3:
  - name: title
    type: text
    authored: yes
    required: yes
    content: 80 characters max
  - name: image
    type: image
    authored: yes
    required: yes
    content: max width 320px, max height 150px
  - name: body
    type: text
    authored: yes
    required: yes
    content: 120 characters max
  - name: tag
    type: text
    authored: yes
    required: "no"
    content: 50 characters max
  - name: link
    type: href
    authored: yes
    required: yes
  - name: link text
    type: text
    authored: yes
    required: yes
    content: 80 characters max

components:
  - title: subscription flag card
    overview: Hierarchical, vertical navigation to place at the side of a page.
    link: /patterns/side-navigation/
    htmlpath: patterns/card/card.md
---

### Each Section
{% include partials/content-specs.md content=page.specs2 %} 

### Each list item
{% include partials/content-specs.md content=page.specs3 %} 

## Functionality Specifications
### Page Header
The page header includes Title and Summary
- max width for summary is 80ex

### Subscribe CTA
The section is on the template and not available through the CMS
- Title: "Stay connected with the latest news and events
- subscription button: label "Subscribe" links to https://public.govdelivery.com/accounts/USACFCWIG/subscriber/new
- manage subscription: link label "Manage your subscriptions" links to https://public.govdelivery.com/accounts/USACFCWIG/subscriber/new

### Body content
h2 - "Learn more about our offerings"

#### For each section
h3 - section title
text - section summary

Uses subscription card flag
- title
- image
- tag
- text
- link & link label

