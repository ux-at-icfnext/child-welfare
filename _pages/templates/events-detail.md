---
layout: template
categories: [templates, events]
type: [detail-page]
title: Events Detail
permalink: /templates/events/detail
overview: The Event Detail page is the destination in the events browsing journey. 
description: The Event Detail page is the destination in the events browsing journey. Please see the [Events](/templates/events) page for information about the Event content type.

prototype:
  - name: Event Detail
    link: https://www.sketch.com/s/dd2f2e71-977c-45b4-baf3-8bf823bfcd0d/p/31BEC0E8-98D7-43D5-B1F3-0FA1F31CFC42/canvas
---

## Page Title
H1 is full width

## Left rail
The left rail is 4 columns wide on the large break points and full width on medium to small breakpoints.
Content:
- event.logo, if available
- website link, "Visit Event Website" (for screen readers add title - "Visit {title} Website"). Link opens in a new window.
- Sub-Section title "Sponsor"
- uses event.sponsor
- Sub-Section title "Date and time"
- uses event.start-date & event.start-time - event.end-date & event.end-time
- Sub-Section title "Location" 
- uses event.type using a tag
- Sub-Section title "Cost"
- uses event.cost
- Sub-Section title "Continuing Education Units"
- uses event.continuing-education-credits

## Right rail
Right rail is 8 columns wide on the large break points and full width on medium to small breakpoints.
Content:
- Section title "About this Event"
- Uses event.summary field
- Sub-Section title "Who Should Attend this Conference"
- Uses event.audience field
- Sub-Section title "Topic tags"
- Uses event.tags - places each item into a clickable tag. 
  - onClick/OnTap of tag, system displays event search page filtered by tag

More from sponsor -- if there are no other events by the sponsor, this section does not display  
- Section Title "More from this Sponsor"
- uses canned link "See all events from {event.sponsor}" 
  - OnClick/OnTap of link, systems displays event search page filtered by sponsor
- uses event-card to display up to 2 events by the same sponsor

[Submission form promo](/patterns/summary-box/submissions) - full width to rail
