---
layout: template
categories: [templates, searchresults]
type: [detail-page]
title: Search Event
permalink: /templates/search-event
overview: Details about the return item for event searches


spec2:
  - name: Event Type
    authored: dynamic
    required: if not available, format type does not display on the item
    type: text + icon
    source: event detail- event type
  - name: Date
    type: text
    authored: dynamic
    content: Displays as "EEE, MON DD, YYYY | HH:MM XM TZD"
    source: event detail- start date & start time & timezone
  - name: Title
    type: h3
    authored: dynamic
    source: event detail- title
  - name: Sponsor
    type: text
    authored: dynamic
    required: if not available, format type does not display on the item
    source: event detail- sponsor
  - name: Summary
    type: text
    authored: dynamic
    content: 250 characters max ~ Note, this cuts the content from the over all summary field
    source: event detail- summary
  - name: link
    type: href
    authored: dynamic
    source: event detail- url

prototype:
  - name: Event Search
    link: /prototype/search/events
---

## Description
The return item module in Event search is similar to the default [search](/templates/searchresults), except that it adds the event date above the event title. And that instead of items from the resource content type it pulls in from the event content type.

## Design Example

![Event Search Item](/assets/icons/spec-images/event-search.png)

## Content Specifications
_uses [collection](/patterns/collection)_
{% include partials/content-specs.md content=page.spec2 %}