---
layout: default
title:  Home Page
categories: [prototype]
type: [sub-nav-item, prototype]
permalink: /prototype/home
summary: This is example of a home page.

alert:
  title: Test alert
  content: Test alert content <a class="usa-link" href="/">see link</a>
  type: info


news:
  settings:
    grid_class: "usa-card--flag tablet:grid-col-6"
    group_class: "usa-card__container__flag-default"
  lists:
  - title: National Adoption Month
    content: Here goes a short description of the urgent promotion, not to exceed 250 characters. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus tortor risus, cursus vitae ante pharetra, pulvinar faucibus nibh. 
    media: "http://placekitten.com/240"
    link_text: Find out more
    link: "#"
  - title: Child Welfare Outcomes Report Released
    content: Here goes a short description of the urgent promotion, not to exceed 250 characters. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus tortor risus, cursus vitae ante pharetra, pulvinar faucibus nibh. 
    media: "http://placekitten.com/240"
    link_text: Read all about it
    link: "#"
  - title: Title Goes Here
    content: Here goes a short description of the urgent promotion, not to exceed 250 characters. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus tortor risus, cursus vitae ante pharetra, pulvinar faucibus nibh. 
    media: "http://placekitten.com/240"
    link_text: Button
    link: "#"
  - title: Adoption Excellence Awards
    content: Here goes a short description of the urgent promotion, not to exceed 250 characters. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus tortor risus, cursus vitae ante pharetra, pulvinar faucibus nibh. 
    media: "http://placekitten.com/240"
    link_text: Check it out
    link: "#"

resources:
  headings:
    title: Just Added
    link: "#"
    link_text: "View all resources"
  settings:
    grid_class: "tablet:grid-col-4"
    group_class: "usa-card__container card-default"
  lists:
    - title: "Social Media: Tips for Youth in Foster Care"
      content: "Card Body - ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae perspiciatis unde omnis iste natus"
      media: http://placekitten.com/300/250
    - title: "Prevention Resource Guide"
      content: "Card Body - ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae perspiciatis unde omnis iste natus"
      media: http://placekitten.com/300/250
    - title: "El cuidado por parientes y el sistema de bienestar de menores (Kinship Care and the Child Welfare System)"
      content: "Card Body - ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium"
      media: http://placekitten.com/300/250

story:
  headings:
    title: News and Stories
    link: "#"
    link_text: "View all news and stories"
  lists:
    - title: "First Item Title Link"
      content: "Learn more about working with families to enhance their capacity to care and protect their children."
      media: https://placekitten.com/200/139
    - title: Second Item Title Link
      content: "Write short description of third item here. Two lines max."
      media: https://placekitten.com/200/139
    - title: Third Item Title Link
      content: "Write short description of third item here. Two lines max."
      media: https://placekitten.com/200/139
    - title: Fourth Item Title Link
      content: "Write short description of third item here. Two lines max."
      media: https://placekitten.com/200/139

overlay:
  settings:
    grid_class: "tablet:grid-col-6"
    group_class: "usa-card__container__campaign overlay"
  lists:
    - title: Child Welfare Information Gateway is Publications
      content: Card Body - Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis earum tenetur quo cupiditate, eaque qui officia recusandae.
      link: "#"
      link_text: "View Resources"
    - title: Stay Connected With Our Free Subscriptions
      content: Card Body - Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis earum tenetur quo cupiditate, eaque qui officia recusandae.
      link: "#"
      link_text: "Subscribe Now"

campaigns:
  headings: 
    title: Campaigns
    link: "#"
    link_text: "View all campaigns"
  settings:
    grid_class: "tablet:grid-col-4"
    group_class: usa-card__container # "usa-card__container__campaign__media overlay"
  lists:
    - title: Campaign Title Here
      content: Ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque.
      media: https://placekitten.com/200/139
    - title: Campaign Title Here
      content: Ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque.
      media: https://placekitten.com/200/139
    - title: Campaign Title Here
      content: Ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque.
      media: https://placekitten.com/200/139

---

{% include patterns/alert/alert-jk.md %}
{% include patterns/hero/hero-landing.md %}

{% include /patterns-jk/card-cta-full.md %}

<div class="grid-container home-news">
  {% include patterns-jk/card-jk.md content=page.news.lists settings=page.news.settings %}
</div>

<section class="home-campaign-hero">
  {% include patterns/hero/hero-campaign-blue.md %}
</section>

<div class="grid-container home-resources">
  {% include patterns-jk/card-group-jk.md content=page.resources.lists settings=page.resources.settings headings=page.resources.headings %}
</div>

<div class="grid-container home-overlay">
  {% include patterns-jk/card-group-jk.md content=page.overlay.lists settings=page.overlay.settings %}
</div>

<section class="campaign-news">
{% include patterns-jk/card-flag-group-jk.md headings=page.story.headings content=page.story.lists %}
</section>

<section class="home-campaigns">
{% include patterns-jk/card-group-jk.md headings=page.campaigns.headings content=page.campaigns.lists settings=page.campaigns.settings %}
</section>

{% include prototype/home/library.md %}









