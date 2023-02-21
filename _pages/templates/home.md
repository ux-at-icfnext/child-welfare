---
layout: template
categories: [templates]
type: [sub-nav-item]
title: Home 
permalink: /templates/home/
overview: This spec will cover the home page template. 
description: The homepage is the door way to the Child Welfare site. As such, it pulls in content from all over. The page is mostly dynamic with a few authorable areas. 

specs:
  - name: title
    type: h1
    authored: yes
    required: yes
    content: 80 characters max
  - name: summary
    type: intro-class
    authored: yes
    required: yes
    content: 120 characters max
  - name: button
    type: text
    authored: yes
    required: yes
    content: 80 characters max
  - name: button-link
    type: url
    authored: yes
    required: yes
  - name: promotion
    type: multi-valuted
    authored: yes
    content: list- title, summary, button-text, button-link, image
  - name: callout
    type: multi-valuted
    authored: yes
    content: list- title, summary, button-text, button-link
---

## Hero
uses [hero](/patterns/hero/)

content: 
- home.title (h1)
- home.summary (usa-intro)
- home.button-text 
- home.button-link 
- home.featured-image

## CTA section
This uses the full version of the CTA cards. See [find help full](/https://dara-icf-cuddly-giggle-pwrjr46q7pg36jwv-4000.preview.app.github.dev/patterns/card/cta-help-full/) & [report full](/https://dara-icf-cuddly-giggle-pwrjr46q7pg36jwv-4000.preview.app.github.dev/patterns/card/cta-report-full/)

## Promotion
The promotion section is collipsible if there are no current promotions. The section can be 1 to 4 cards. 
- Section Title (h2) home.promotion-heading
- Each card
  - home.promotion-title
  - home.promotion-summary
  - home.promotion-button-text
  - home.promotion-button-link
  - home.promotion-image

## Campaign
uses [hero-right](/patterns/hero-campaign-blue/)

The campaign section is collipsible if there are no campaigns. There are two parts to this section, the current running campaign and a place to put a future campaign.

Hero content:
- campaign.title (h2)
- campaign.summary (usa-intro)
- campaign.button-text
- campaign.button-link
Future compaign content:
- title (h3) - "Comming Soon"
- campaign.title (h4)
- campaign.button-text
- campaign.button-link

## Just Added
uses [usa-card with media](/patterns/card/card-with-media/)

The just addes section shows the most recent resources. With a link to view all resources.

Section Title: "Just Added" (h2)

Link Content:
- "View all Resources"
- Links to the all resources page
Cards Content:
- resource.title
- resource.summary
- resource.thumbnail
- button text should be "read more" ... with aria text as "read more about {resource.title}"
- button url - resource.url

## Call Out Section
uses [card-campaign](/patterns/card/card-campaign/)

_limit 2_

- home.callout-title
- home.callout-summary
- home.callout-button-text
- home.callout-button-link

## Explore Topics and Series
uses [card-flag](/patterns/card/card-flag-default/) -- which is responsive to card-wide as their container becomes smaller than 480px. The first card 12 columns, while the following 3 cards are four columns.

Title: "Explore our Topics" (h2)

Link Content:
- "View all Topics"
- Links to the Topics Landing page
Cards Content:
- topic.title (links to distination page using topic url)
- topic.thumbnail
- topic.summary


## Initivies
uses [card-campaign](/patterns/card/card-campaign/) with the 3 most recent campaigns

Title: TBD

Link Content:
- "View all campaigns"
- Links to an authored campaign page using the "series" template
Cards Content:
- campaign.title
- campaing.summary
- campaign.url

## Explore our Library
- Title "Explore our Library"
- Summary - TBD
- Search ... uses [search widget](/patterns/search/) ... on click of search, search parameters are sent to the library search.





