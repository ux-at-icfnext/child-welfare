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
    media: /assets/icons/images/nam2022.jpg
    link_text: Find out more
    link: "#"
  - title: Child Welfare Outcomes Report Released
    content: Here goes a short description of the urgent promotion, not to exceed 250 characters. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus tortor risus, cursus vitae ante pharetra, pulvinar faucibus nibh. 
    media: /assets/icons/images/cwo-report.jpg
    link_text: Read all about it
    link: "#"
  - title: Title Goes Here
    content: Here goes a short description of the urgent promotion, not to exceed 250 characters. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus tortor risus, cursus vitae ante pharetra, pulvinar faucibus nibh. 
    media: /assets/icons/images/500_F_119210748.jpg
    link_text: Button
    link: "#"
  - title: Adoption Excellence Awards
    content: Here goes a short description of the urgent promotion, not to exceed 250 characters. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus tortor risus, cursus vitae ante pharetra, pulvinar faucibus nibh. 
    media: /assets/icons/images/aea_award.jpg
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
      media: /assets/icons/images/SMTips-Youth2.jpg
    - title: "Prevention Resource Guide"
      content: "Card Body - ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae perspiciatis unde omnis iste natus"
      media: /assets/icons/images/ncapma-rg.jpg
    - title: "El cuidado por parientes y el sistema de bienestar de menores (Kinship Care and the Child Welfare System)"
      content: "Card Body - ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium"
      media: /assets/icons/images/SMTips-Caregiver2.jpeg

story:
  headings:
    title: News and Stories
    link: "#"
    link_text: "View all news and stories"
  lists:
    - title: "First Item Title Link"
      content: "Learn more about working with families to enhance their capacity to care and protect their children."
      media: /assets/icons/images/family-practice.jpg
    - title: Second Item Title Link
      content: "Write short description of third item here. Two lines max."
      media: /assets/icons/images/500_F_306140481.jpg
    - title: Third Item Title Link
      content: "Write short description of third item here. Two lines max."
      media: /assets/icons/images/medical.jpg
    - title: Fourth Item Title Link
      content: "Write short description of third item here. Two lines max."
      media: /assets/icons/images/1000_F_135780146.jpeg

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
      campaign-class: usa-card__container__campaign-one
    - title: Campaign Title Here
      content: Ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque.
      media: https://placekitten.com/200/139
      campaign-class: usa-card__container__campaign-two
    - title: Campaign Title Here
      content: Ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque.
      media: https://placekitten.com/200/139
      campaign-class: usa-card__container__campaign-three

---
<style>
  .home-resources{
    margin-top: 4rem;
  }
  .home-overlay{
    margin-top: 1rem;
  }
  .campaign-news{
    margin-top: 1rem;
  }
  .home-campaigns{
    margin-top: 1rem;
    margin-bottom: 1rem;
  }
</style>

{% include patterns/alert/alert-jk.md %}
{% include patterns/hero/hero-landing.md %}

{% include /patterns-jk/card-cta-full.md %}

<div class="grid-container home-news">
  {% include patterns-jk/card-jk.md content=page.news.lists settings=page.news.settings %}
</div>

<section class="home-campaign-hero">
  {% include patterns/hero/hero-campaign-blue.md %}
</section>

<div class="grid-container home-resources" style="margin-top: 4rem;">
  {% include patterns-jk/card-group-jk.md content=page.resources.lists settings=page.resources.settings headings=page.resources.headings %}
</div>

<div class="grid-container home-overlay" style="margin-top: 1rem;">
  {% include patterns-jk/card-group-with-button-jk.md content=page.overlay.lists settings=page.overlay.settings %}
</div>

<section class="campaign-news" style="margin-top: 1rem;">
{% include patterns-jk/card-flag-group-jk.md headings=page.story.headings content=page.story.lists %}
</section>

<section class="home-campaigns" style="margin-top: 1rem; margin-bottom: 1rem;">
{% include patterns-jk/card-group-campaign.md headings=page.campaigns.headings content=page.campaigns.lists settings=page.campaigns.settings %}
</section>

{% include prototype/home/library.md %}








