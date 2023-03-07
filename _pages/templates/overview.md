---
layout: template
categories: [templates, overview-page]
type: [sub-nav-item]
title: Overview Landing
permalink: /templates/overview-page
overview: Groups subtopic/resources pages together according to topic

description: |
  The topic page is used to group subtopic pages together. It is also used to group series together, where the destination pages are resources. The top portion of the page allows the author to explain the grouping that they've created.

components:
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
  - name: Filter Criteria
    type: taxonomy terms
    authored: yes
    required: yes
    notes: author must choose the taxonomy terms that are applied to this page.
  - name: Featured List
    subhead: yes
    type: usa-card
    authored: yes
    required: yes
    content: limit 3
    notes: each list item - title, text, link
  - name: Featured Label
    type: h2
    authored: yes
    content: 80 characters max
    notes: default text "Featured"
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
  - name: List
    subhead: yes
    type: usa-card
    authored: yes
    required: yes
    content: limit 9 - multi-valued, see below
  - name: Topics label
    type: h2
    content: "Subtopics"
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
  - name: Related
    subhead: yes
    type: usa-accordion
    content: multi-valued text-card
    notes: front-end only, no need to store the accordion in drupal (only the linked references)
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


prototype:
  - name: Overview
    link: https://www.sketch.com/s/dd2f2e71-977c-45b4-baf3-8bf823bfcd0d/a/3OLlxQw#Inspect
---

## Functionality Specifications
### Page Header
The pages uses a full width image hero across the top. Followed by the page title (h1) and body content (max width 80ex). 
- note: the summary text is used only as the page meta data

### Page Features
The features contain a section header (h2) and the maximum of 3 featured items.
- the features uses [usa-card with media](/card-with-media/)
- on smaller breakpoints the cards stack 
- on larger breakpoints the cards spread 3 across
- see table above for the content parts

### Subtopics
The subtopic contain a section header (h2) and the subtopic items.
- the subtopic uses [usa-card](/card/)
- on smaller breakpoints the cards stack 
- on larger breakpoints the cards spread 3 across
- see table above for the content parts

### Related Series
The related series contains a section title (h2) and the related items. 
- The section title has a full width blue bar behind it and a blue border surrounds the other 3 sides of the section.
- The related items uses the [text card](/card-text) and uses a column design so that items fall naturally under the item above (not aligned to the items left or right.). 
- On large screens fits 3 columns, on medium on 2 columns, on small fits 1 column.

