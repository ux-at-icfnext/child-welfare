---
layout: template
categories: [templates, search]
type: [sub-nav-item, variations]
title: Search
permalink: /templates/search
overview: Search pages are mostly dynamic.
description: Search pages are mostly dynamic, there are several search pages through out the site. These include, the Global Search, All Resources, Event Search, Directory, and Subtopics. They all share the same basic functionality.

spec2:
  - name: Page Title
    type: h1
    required: true
    authored: true
  - name: Summary
    type: meta description
    content: 250 characters max
    required: true
    authored: true
  - name: Body
    type: rich text
    content: 200 word max recommended
  - name: Pullquote
    type: multi-valued
    content: see table below
  - name: Quicklinks
    type: multi-valued
    content: see table below


      
---

### Search Page functionality – onLoad
On page load, content is sorted by Latest Published and 15 items are displayed.
There are three types of incoming searches, canned, keyword, empty.

#### Empty -
a user submits an empty search (search from with blank input field)
In this instance, the search page is displayed without out any filters applied.

#### Keyword -
Any search using the search module, results are constrained to keyword matches.

#### Canned -
Authors should be able to create links in the site to a prefiltered search result. For this functionality to work, search terms and filters need to be added to the url.

### Page Header
_note_ [Subtopics Pages](templates/subtopic-page) has it's own page header. Please see the specifications for how that page functions.

{% include partials/content-specs.md content=page.specs2 %}


