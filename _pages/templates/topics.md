---
layout: template
categories: [templates, topics-page]
type: [sub-nav-item]
title: Topics
permalink: /templates/topics-page
overview: Groups subtopic/resources pages together according to topic

description: |
  The topic page is used to group subtopic pages together. It is also used to group series together, where the destination pages are resources. The top portion of the page allows the author to explain the grouping that they've created.

compontents:
  - title: Image hero
    link: /patterns/hero-image/ 
  - title: usa-card
    link: /patterns/card/card/
  - title: usa-card-with-media
    link: /patterns/card/card-with-media/
  - title: Text Cards
    link: /patterns/card/cards-text/

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
    notes: meta tags only -- does not show on page
  - name: Body
    type: rich text
    authored: yes
    required: yes
    content: reccommended 200 word max
    searchable: yes
    notes: allows h2, h3, h4, bullets, links, icons
  - name: Hero image
    type: image
    required: yes
    content: 1400x400 pixels
    authored: yes
  - name: Featured Label
    type: h2
    authored: yes
    content: 80 characters max
    notes: default text "Featured"
  - name: Featured List
    type: usa-card
    authored: yes
    required: yes
    content: limit 3
    notes: each list item - title, text, link
  - name: Topics label
    type: h2
    authored: yes
    content: 80 characters max
    notes: default text "Subtopics" or "Series" on series pages
  - name: List
    type: usa-card
    authored: yes
    required: yes
    content: limit 9 - multi-valued, see below
  - name: Related
    type: usa-accordion
    authored: no
    content: multi-valued text-card
    notes: front-end only, no need to store the accordion in drupal (only the linked references)


specs2:
  - name: Title
    type: h3
    authored: dynamic
    source: destination page -  title
  - name: image
    type: image
    authored: dynamic
    source: destination page - hero image
    notes: 
  - name: body
    type: text
    authored: dynamic
    source: destination page - summary
  - name: link
    type: href
    authored: dynamic
    source: destination page - url

specs3:
  - name: Title
    type: h3
    authored: dynamic
    source: destination page -  title
  - name: body
    type: text
    authored: dynamic
    source: destination page - summary
  - name: link
    type: href
    authored: dynamic
    source: destination page - url

prototype:
  - name: Topics
    link: https://www.sketch.com/s/dd2f2e71-977c-45b4-baf3-8bf823bfcd0d/a/3OLlxQw#Inspect
---
