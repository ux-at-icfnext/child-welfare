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
    group_class: "card-default usa-card--flag"
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
---

{% include patterns/alert/alert-jk.md %}
{% include patterns/hero/hero-landing.md %}

<div>{% include patterns/card/card-cta-help-full.md %}</div>
<div>{% include patterns/card/card-cta-report-full.md %}</div>

<section class="news">
{% include patterns-jk/card-jk.md content=news.lists settings=news.settings %}
</section>






