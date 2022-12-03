---
layout: template
categories: [templates, resource-detail]
type: [sub-nav-item, variations]
title: Resource Detail Page
permalink: /templates/resource-detail-page
overview: This template is used for housing all the sites resources.

description:  This template is used for housing all the sites resources. There are small variations based on the type of resource being viewed. The different resource modules are discribed in the child pages.

specs:
  - name: Title
    type: h2
    authored: yes
    required: yes
    content: 80 characters max
    searchable: yes
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
  - name: List link
    type: href
    authored: yes
    required: yes
---