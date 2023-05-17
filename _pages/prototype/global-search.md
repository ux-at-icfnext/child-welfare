---
layout: default
title: Search Results
categories: [prototype]
type: [sub-nav-item, prototype]
permalink: /prototype/search
overview: Search results page
summary: Search results page
search_type: all
breadcrumbWrapping: true

body: |
  Body copy- several sentences’ worth. Quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut et via procedat oratio quaerimus igitur, inquit, modo dixi, constituto, ut earum motus et iusto odio.

---
{% include patterns/breadcrumb/breadcrumb-jk.md %}
<div class="grid-container" markdown="1">

</div>

<div class="grid-container" markdown="1">
# {{ page.title }}

<div class="grid-row grid-gap-lg" markdown="1" style="margin-bottom: 60px;">
  <p>{{ page.body }}</p>
</div>
</div>

{% include prototype/search-results.md %}


