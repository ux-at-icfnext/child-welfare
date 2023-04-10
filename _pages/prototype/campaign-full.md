---
layout: default
title: Campaign Landing page
categories: [prototype]
type: [sub-nav-item, prototype]
permalink: /prototype/campaign/2
summary: This is example of a campaign page.

hero:
  - title: Campaign Name
    content: "Campaign Subtitle, consisting of a short description of the campaign. This can be two to three lines in length."
    link_text: Get Involved
    media: /assets/icons/images/full-image-hero.jpg
    alt: placeholder image
    media-class: usa-card__media--inset

news:
  headings:
    - title: News and Stories
      link: "#"
      link_text: "View all news and stories" 
---
{% include patterns/breadcrumb/breadcrumb-jk.md %}
{% include patterns/hero/hero-full-width-jk.md content=page.hero %}

{% include prototype/campaign/impact_pie.md %}
{% include prototype/campaign/news_stories.md %}
{% include prototype/campaign/involved_vision.md %}
{% include prototype/campaign/resources.md %}
