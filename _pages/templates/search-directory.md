---
layout: template
categories: [templates, searchresults]
type: [detail-page]
title: Search Directory
permalink: /templates/search-directory
overview: Details about the return item for directory searches

spec2:
  - name: Title
    type: h3 link
    authored: dynamic
    source: directory detail-title
  - name: Link
    type: href
    authored: dynamic
    source: directory detail-url
  - name: Email
    type: email
    authored: dynamic
    source: directory detail-email
  - name: Contact form Link
    type: href
    content: Link will display with text "Contact Form"
    authored: dynamic
    source: directory detail-form link
  - name: Address
    type: text
    authored: dynamic
    source: directory detail-address
  - name: Address 2
    type: text
    authored: dynamic
    source: directory detail-address 2
  - name: City
    type: text
    authored: dynamic
    source: directory detail-city
  - name: State
    type: text
    authored: dynamic
    source: directory detail-state
  - name: Zip
    type: text
    authored: dynamic
    source: directory detail-zip
  - name: Summary
    type: text
    authored: dynamic
    source: directory detail-summary
  - name: Primary function
    type: text
    authored: dynamic
    content: displays with label "Primary Function(s):"
    source: directory detail-functions
  - name: Social
    type: icon links
    authored: dynamic
    source: directory detail-social
  


---

## Description
The return item module in Directory search pulls in from the directory content type.


## Design Example
![design example for directory](/assets/icons/spec-images/directory-search.png)

## Content Specifications
_uses [collection](/patterns/collection)_
{% include partials/content-specs.md content=page.spec2 %}