---
layout: template
categories: [templates, resource-detail]
type: [sub-nav-item, variations]
title: Resource Detail Page
permalink: /templates/resource-detail-page
overview: This template is used for housing all the sites resources.

description:  The Resource Detail template houses various resources types that all have their own required aspects. On this overview page, you will see the common functionaly and content types. The requirements for each resource type will be linked in a sub-page.


specs:
  - name: Title
    type: h2
    authored: yes
    required: yes
    content: 80 characters max
    searchable: yes
  - name: Summary
    type: meta tags
    authored: yes
    required: yes
    content: 250 characters max
    notes: used in meta tags only
  - name: Date
    type: date
    authored: yes
    required: yes
    content: shows date format "Month DD, YYYY"
  - name: Length
    type: time
    content: lenth of video or podcast format "hh:mm:ss"
  - name: Opening Body
    type: rich text
    authored: yes
    content: reccommended 150 word max
    searchable: yes
    notes: allows h2, h3, h4, bullets, links, icons
  - name: resource item
    content: types - podcast, video, publication, webinar
    notes: read sub pages for each specification for each type
  - name: Body
    type: rich text
    authored: yes
    searchable: yes
    notes: allows h2, h3, h4, bullets, links, icons, quotes
  - name: Series
    type: list
    content: multivalued - see table below
  - name: Related
    type: list
    content: multivalued - see table below
  - name: Filter Criteria
    type: taxonomy terms
    authored: yes
    required: yes
    notes: author must choose the taxonomy terms that are applied to this page.

specs2: 
  - name: List text
    type: text
    authored: yes
    required: yes
    source: distation page title
  - name: List link
    type: href
    authored: yes
    required: yes
    source: distation page url
---

### Series list item
{% include partials/content-specs.md content=page.specs2 %} 

### Related list item
{% include partials/content-specs.md content=page.specs2 %} 

## Functionality Specifications
This section show the details on how to build the page based on the author selections.

### Page Header
The page header includes the page title (h1), date, and length and opening body.
- The date label changes by type of resource... please see the resource pages for which date label. (Options include:"Date Published", "Current through Date", "Event Date")
- The body has a max-width of 80ex

### Resource Item
See variations below.

### Body
- Rich text (includes option for pull quotes)
- Max-width 80ex

## Series Links
Resources are linked dynamically by series. Displays up to 5 resources to features from this series.
- Module title - h2 - content: "Also in this series"
- list - page title of related resource - link options to resource page
- url - page link of related resource

## Related Resourcs
Authors can choose up to 9 resources to features from this series.
- Module title - h2 - content: "Related Resources"
- list - page title of related resource - link options to resource page
- url - page link of related resource