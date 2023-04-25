---
layout: default
title: Campaign Landing page
categories: [prototype]
type: [sub-nav-item, prototype]
permalink: /prototype/campaign/1
summary: This is example of a campaign page.

cards:
  settings:
    group_class: "usa-card_container card-default"
  lists:
    - title: "Social Media: Tips for Youth in Foster Care"
      content: | 
        Card Body - ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae perspiciatis unde omnis iste natus  
      link_text: More on social media tips
      media: /assets/icons/images/SMTips-Youth2.jpg
      alt: placeholder image
      class: tablet:grid-col-4
    - title: "Prevention Resource Guide"
      content: | 
        Card Body - ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae perspiciatis unde omnis iste natus   
      link_text: More on prevention
      media: /assets/icons/images/ncapma-rg.jpg
      alt: placeholder image
      class: tablet:grid-col-4
    - title: "El cuidado por parientes y el sistema de bienestar de menores (Kinship Care and the Child Welfare System)"
      content: | 
        Card Body - ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium…  
      link_text: More on El cuidado por parientes
      media: /assets/icons/images/SMTips-Caregiver2.jpeg
      alt: placeholder image
      class: tablet:grid-col-4
events:
  headings:
    title: Events
    link: "#"
    link_text: "See All Campaign Events"
  settings:
    group_class: "event-card card-default"
  lists:
    - title: "Living The Protective Factors"
      tag: virtual
      content: "Thu, Nov 18,2023 | 11am ET"
      link_text: Be Strong Families
    - title: "Recognizing and Responding to Family Stress"
      tag: virtual
      content: "Thu, Nov 18,2023 | 11am ET"
      link_text: Be Strong Families
    - title: "How We endUP: A Future Without Family Policing"
      tag: call
      content: "Thu, Nov 18,2023 | 11am ET"
      link_text: The upEND Movement
    - title: "Living The Protective Factors"
      tag: New York, NY
      content: "Thu, Nov 18,2023 | 11am ET"
      link_text: Living The Protective Factors
    - title: "Recognizing and Responding to Family Stress"
      tag: hybrid
      content: "Thu, Nov 18,2023 | 11am ET"
      link_text: Living The Protective Factors
    - title: "How We endUP: A Future Without Family Policing"
      tag: virtual
      content: "Thu, Nov 18,2023 | 11am ET"
      link_text: The upEND Movement
    

      
---
<style>
  .usa-card__media{
    order: 0;
  }
  .usa-card__body{
    margin-top: 1rem;
    padding-bottom: 1rem;
  }
</style>

{%include patterns/breadcrumb/breadcrumb-basic.md%}

{% include patterns/hero/hero-campaign-white.md %}

{% include prototype/campaign/misson.md %}
{% include prototype/campaign/impact.md %}
{% include prototype/campaign/involved.md %}
{% include prototype/campaign/events.md %}
{% include prototype/campaign/goals.md %}
{% include prototype/campaign/related.md %}