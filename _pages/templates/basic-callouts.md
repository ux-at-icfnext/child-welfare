---
### This is now archived
layout: template
categories: [templates, topics-page]
# type: [sub-nav-item]
title: Basic with Callouts
permalink: /templates/callouts-page
overview: A basic type page that allows for feature callouts at the top

description: |
    Use this basic with call out pages for when you need to have featured items at the top of the page.  A good example use case is the "How to Report Child Abuse" page where important information needs to be readily available at to top.

prototypes:
 - name: Example - How to Report Child Abuse
   link: https://www.sketch.com/s/dd2f2e71-977c-45b4-baf3-8bf823bfcd0d/a/agRLDQp

components:
    - title: card-alert
      link: /patterns/card/card-alert
    - title: card-cta
      link: /patterns/card/card-cta-help

specs: 
    - name: Title
      type: h1
      authored: yes
      required: yes
      content: 80 characters max
      searchable: yes
    - name: Summary
      type: text (usa-intro)
      authored: yes
      required: yes
      content: 250 characters max
      searchable: yes
    - name: Callouts
      type: list
      authored: yes
      required: yes
      content: multi-valued, see table below
      notes: CMS should use a list to create
    - name: Body
      type: rich text
      authored: yes
      required: yes
      notes: allows h2, h3, h4, bullets, links, icons
    - name: CTAs
      type: multi-select
      content: uses the "find Help" & "Report" cta cards
      note: author should be able to chose to show one or both cards
      


specs2: 
    - name: Title
      type: h2
      authored: yes
      required: yes
      content: 80 characters max
    - name: Text
      type: text
      authored: yes
      required: yes
      content: 250 characters max
      searchable: yes
    - name: button text
      type: button
      authored: yes
      required: yes
      content: 50 characters max 


---

## Each Callout
uses card-alert
{% include partials/content-specs.md content=page.specs2 %}


## Functionality Specifications
### Page Header
- page title (h1)
- page summary (class: usa-intro)

### Call outs
uses card-alert 3 cards (min/max)
- on smaller breakpoints the cards stack 
- on larger breakpoints the cards spread 3 across
- see table above for the content parts

### Page body
Max width is 80 ex
Optional cta cards shown on bottom. If a single card it should be full width, 2 cards would be side by side on the larger breakpoints.


### For the "How to Report Child Abuse" page 
This page uses the [Quick Exit](/patterns/quick-exit) functionality. Read more on the [pattern specifications](/patterns/quick-exit) page.

