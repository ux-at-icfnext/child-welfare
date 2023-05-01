---
layout: template
categories: [templates, topic]
type: [sub-nav-item]
title: Topic & Subtopic 
permalink: /templates/topic/
overview: Group resources according to topic categories.


description: |
  The topic page is used to group a set of resources according to a category. The top portion of the page allows the author to explain the grouping and elevate resources in the featured area. If the page is a Topic page, it pulls in a list of subtopic pages. The bottom section of the page is a dynamically feed search result. 
details:
components:
  - title: Landing Page hero
    link: /patterns/hero-landing/
  - title: Cards
    link: /patterns/card/
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
  - name: Parent Topic
    type: dropdown
    notes: allows author to connect a subtopic to a topic
  - name: Filter Criteria
    type: taxonomy terms
    authored: yes
    required: yes
    notes: author must choose the taxonomy terms that are applied to this page.
  - name: Subtopics
    type: h2
    content: "Subtopics"
    notes: is the page is a topic page (the parent topic field is empty -- show this section title)
  - name: Subtopic list
    subhead: yes
    type: card
    content: multi-valuded
    notes: uses list to create subtopics using content that uses this page in the parent field
  - name: Title
    type: h3
    content: "source: topic - title"
  - name: Summary
    type: text
    content: "source: topic - summary"
  - name: Featured Label
    type: h2
    authored: yes
    content: 80 characters max
    notes: default text "Featured"
  - name: List
    subhead: yes
    type: usa-card
    authored: yes
    required: yes
    content: limit 9 - multivalued
    notes: there needs to be a mechanism for authors to choose these features from a list of resources.
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
  - name: Topic
    link: /prototype/topic-example-youth/
  - name: Subtopic 
    link: /prototype/subtopic-ex-engaging-and-involving-youth/
---


## Functionality Specifications
This section show the details on how to build the page based on the author selections.

### Page header
The page header uses the [landing hero](/patterns/hero-landing) pattern. This includes the page title (h1) and the hero image.
* note: the summary text is used only as the page meta data 

### Page Body
If the page is a Topic page (the parent field is empty), then use [usa-card](/card) to show the subtopics (pages with this page as a parent). 
- Section title is the h2
- Cards show in a gallery layout, with 3 cards across at the maximum width / 1 card across on the smallest width.


### Featured Block
Feature title is the h2.

The features uses the [text card](/patterns/card/cards-text/) pattern. The cards are layout using a mosaic style. 
- The features are limited to 6 returns.
- The title (h3) links to the url destination.

### Search
The rest of the page is a canned search result where the returns are constrained to the filter criteria field. 

Please seach[Search](/templates/searchresults) for more information on how Search works.