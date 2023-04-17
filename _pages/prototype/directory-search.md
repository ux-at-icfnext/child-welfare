---
layout: default
title: Directory
categories: [prototype]
type: [sub-nav-item, prototype]
permalink: /prototype/search/directory
overview: Directory search results page
summary: Directory search results page
search_type: directory

body: |
  Body copy- several sentences’ worth. Quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut et via procedat oratio quaerimus igitur, inquit, modo dixi, constituto, ut earum motus et iusto odio.
  > If you would like to join the directory, update your listing, or if you have any question
  > - <i class="fa-kit fa-mail"></i>[nfcadupdates@childwelfare.gov](#) <i class="fa-kit fa-phone"></i>[800.394.3366](#)

summary-title: Quick links
summary-class: quick-links
summary-list:
  - item: <a href="/">How to become a foster parent</a>
  - item: <a href="/">How to adopt </a>
  - item: <a href="/">Contact information for local and county childwelfare agencies </a>
  - item: <a href="/">Accredited/approved adoption services providers for intercountry adoption <i class="fa-kit fa-launch"></i> </a>
  
---

<div class="grid-container" markdown="1">
# {{ page.title }}

<div class="grid-row grid-gap-lg" markdown="1">
  <div class="grid-col-6"> {{ page.body | markdownify }} </div>
  <div class="grid-col-6"> {% include patterns/summary-box/summary-box-jk.md %} </div>
</div>
</div>

{% include prototype/search-results.md %}

