---
layout: template
categories: [templates, subtopic-page]
type: [sub-nav-item]
title: Subtopic 
permalink: /templates/subtopic-page/
overview: Group resources according to a subtopic category.


description: |
  The subtopic page is used to group a set of resources according to a category. The top portion of the page allows the author to explain the grouping and elevate resources in the featured area. The bottom section of the page is a dynamically feed search result. All subtopic pages are grouped by [Topic](/templates/topic-page).
details:
components:
  - title: Landing Page hero
    link: /patterns/hero-landing/
  - title: Text Cards
    link: /patterns/card/cards-text/
  - title: Search
    link: /templates/searchresults


specs:
  - name: Title
    type: h1
    authored: yes
    required: yes
    content: 80 characters max
    searchable: yes
  - name: Hero image
    type: image
    authored: yes
    required: yes
    content: ratio 3:2 (645 x 430 on desktop)
  - name: Summary
    type: meta data
    authored: yes
    required: yes
    content: 250 characters max
    searchable: yes
  - name: Body
    type: rich text
    authored: yes
    required: yes
    searchable: yes
    content: suggested max length 200 words.
    notes: allows h2, h3, h4, bullets, links, icons
  - name: Featured Label
    type: h2
    authored: yes
    content: 80 characters max
    notes: default text "Featured"
  - name: List
    type: usa-card
    authored: yes
    required: yes
    content: limit 9 - multivalued
    notes: there needs to be a mechanism for authors to choose these features from a list of resources.
  - name: Filter Criteria
    type: taxonomy terms
    authored: yes
    required: yes
    notes: author must choose the taxonomy terms that are applied to this page.

specs2:
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
  - name: Subtopic 
    link: https://www.sketch.com/s/dd2f2e71-977c-45b4-baf3-8bf823bfcd0d/a/pazwK8G
---

### Each list item
{% include partials/content-specs.md content=page.specs2 %} 

## Functionality Specifications
This section show the details on how to build the page based on the author selections.

### Page header
The page header uses the [landing hero](/patterns/hero-landing) pattern. This includes the page title (h1) and the hero image.
* note: the summary text is used only as the page meta data 

### Page Body
The page body contains the body, accordions and vertical tabs. All of these elements are optional, although the author can choose either the accordion or the vertical tabs, not both.
- the body displays first with a max-width of 80ex.
- the author can choose either the accordion or the vertical tabs, not both. The list content is used to fill the pattern using the label, title (h2), and content.

### Featured Block
Feature title is the h2.

The features uses the [text card](/patterns/card/cards-text/) pattern. The cards are layout using a mosaic style. 
- The features are limited to 6 returns.
- The title (h3) links to the url destination.

### Search
The rest of the page is a canned search result where the returns are constrained to the filter criteria field. 

Please seach[Search](/templates/search) for more information on how Search works.