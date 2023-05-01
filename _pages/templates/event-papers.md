---
### This is now archived
layout: template
categories: [templates, events]
# type: [detail-page]
title: Call For Papers Detail
permalink: /templates/events/papers
overview: The Call for Papers Detail page is the destination in the events browsing journey. 
description: The Call for Papers Detail page is the destination in the events browsing journey. Please see the [Events](/templates/events) page for information about the Event content type.

---

## Page Title
H1 is full width

## Left rail
The left rail is 4 columns wide on the large break points and full width on medium to small breakpoints.
Content:
- event.logo, if available
- website link, "Visit Sponsor Website". Link opens in a new window.
- Sub-Section title "Sponsor"
- uses event.sponsor
- Sub-Section title "Deadline"
- uses event.start-date & event.start-time
- uses event.type using a tag

## Right rail
Right rail is 8 columns wide on the large break points and full width on medium to small breakpoints.
Content:
- Section title "About this Call for Papers"
- Uses event.summary field
- Section title "Contact Information"
- Uses "Phone:" event.phone "Email:" event.email
- Sub-Section title "Eligibility"
- Uses event.audience field
- Sub-Section title "Topic tags"
- Uses event.tags - places each item into a clickable tag. 
  - onClick/OnTap of tag, system displays event search page filtered by tag


[Submission form promo](/patterns/summary-box/submissions) - full width to rail
