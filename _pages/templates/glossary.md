---
layout: template
categories: [templates]
type: [sub-nav-item]
title: Glossary 
permalink: /templates/glossary/
overview: This spec will cover the glossary page template. 
description: The homepage is the door way to the Child Welfare site. As such, it pulls in content from all over. The page is mostly dynamic with a few authorable areas. 

specs:
  - name: Title
    type: h1
    content: "Glossary"
  - name: Summary
    type: text
    content: 250 words maximum
    required: yes
    authored: yes
  - name: Terms
    subhead: yes
  - name: Term Name
    type: Text
    authored: yes
    required: yes
  - name: Term Name Spanish
    type: text
    authored: yes
    content: "state Spanish like -- {spanish term} (Spanish)"
  - name: body
    type: text
    authored: yes
    required: yes
  - name: Link text
    type: text
    authored: yes
  - name: Link
    type: url
    authored: yes

prototype:
  - name: Glossary
    link: /prototype/glossary
---

## Functional Specifications
OnPage load, result is sorted alphabetically, limit 20 results per page.

### Page Layout
- Title - h1
- Summary -- usa-intro
- 45% of width on large+ breakpoints & side by side with navigation -- 98% medium- breakpoints, stacks
  - Search 
  - A to Z navigation
- term results
- pagination

### Search
OnSubmit of term, system displays result set where the keyword entered matches the term name.

### A to Z navigation
OnClick/OnTap of letter, system displays the result set of terms that start with selected letter. Results are sorted alphabetically. Limit 20 per page.

### Term results
- Term Name 
- Term Name Spanish... formatted as "{term-name} (Spanish)"
- Body
- Link to source (link text/link) (note uses usa-icon launch if external)

### Pagination
Result set is limited to 20 per page. Pagination works in accordance with the [specifications](patterns/pagination/)