---
### This is now archived
layout: template
categories: [templates, events]
# type: [detail-page]
title: Events / Call For Papers Form
permalink: /templates/events/form
overview: The Event form allows organizations to add their events or call for papers. 
description: |
  # THIS IS STILL IN DRAFT!!
  The Event form allows organizations to add their events or call for papers. The form is four pages in all. Some of the labeling varies on the Call To Papers form... the tables below make these differences clear. Please see the [Events](/templates/events) page for information about the Event content type. 

prototype:
  - name: Forms
    link: https://www.sketch.com/s/dd2f2e71-977c-45b4-baf3-8bf823bfcd0d/p/F65FADAF-0F3B-4197-83B1-6BE9B808899B/canvas

page1:
  - name: Event Type
    field: "drop-down - Options: Virtual, In-person, Hybrid, Call for Papers"
    required: yes
    content: event.event-type
    error: "Please select the type of event this is"
  - name: Title (80 characters)
    field: "input -  80 charactes maximum"
    required: yes
    content: event.title
    error: "Please enter a name for your event"
  - name: Sponsor


---

## Form Structure
- All required fields show a red "*" after the label and on Submit must pass error validation.
- Some of the 

{% include /partials/event-specs.md content=page.page1 %}