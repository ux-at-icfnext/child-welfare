---
layout: default
title: Events Search
categories: [prototype]
type: [sub-nav-item, prototype]
permalink: /prototype/search/events
overview: Event search results page
summary: Event search results page

body: |
  Body copy- several sentences’ worth. Quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut et via procedat oratio quaerimus igitur, inquit, modo dixi, constituto, ut earum motus et iusto odio.

summary-title: Submit Events and Calls for Papers
summary-class: submissions
summary-list:
  - item: Submit information on your events. We will then post your submission to this website.
  - item: <a href="/">Fill in a submission form </a>
---

<div class="grid-container" markdown="1">
# {{ page.title }}

<div class="grid-row grid-gap-lg" markdown="1">
  <div class="grid-col-6"> {{ page.body }} </div>
  <div class="grid-col-6"> {% include patterns/summary-box/summary-box-jk.md %} </div>
</div>
</div>

{% include prototype/search-results.md %}

