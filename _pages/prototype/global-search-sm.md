---
layout: default
title: Search Results
categories: [prototype]
type: [sub-nav-item, prototype]
permalink: /prototype/search/sm
overview: Search results page
summary: Search results page
search_type: all
search-type: small
search_placeholder: "Search by keyword"
breadcrumbWrapping: true
body: |
  Body copy- several sentences’ worth. Quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut et via procedat oratio quaerimus igitur, inquit, modo dixi, constituto, ut earum motus et iusto odio.

---
<div class="grid-container" markdown="1">
{% include patterns/breadcrumb/breadcrumb-jk.md %}
</div>

<div class="grid-container" markdown="1">
# {{ page.title }}

<div class="grid-row grid-gap-lg" markdown="1">
  {{ page.body }} 
</div>

{% include patterns/search/search-jk.md %}

<div class="grid-row grid-gap-lg">
  <div class="grid-col">{% include prototype/search/filter-accordions-sm.md %}</div>
  <div class="grid-col"> 
    <select class="usa-select" style="height: 56px;top: -8px; position: relative;" name="view" id="view">
        <option value="Relevance">Relevance</option>
        <option value="Latest Published">Latest Published</option>
        <option value="A-Z">A-Z</option>
      </select>
  </div>
</div>
{% include prototype/search/filter-display.md %}

<div class="applied-filters" style="padding-bottom: 2rem;">
    <span class="text-bold">Applied Filters:</span><span class="usa-tag">All Resource Types <i class="fa-kit fa-close"></i></span>
</div>

<div class="return-list">
    {% for i in (1..5) %}
    {% include prototype/search/return-list.md %}
    {% endfor %}
</div>
{% include patterns/pagination/pagination.md %}


</div>

