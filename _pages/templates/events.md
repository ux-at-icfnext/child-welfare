---
layout: left-rail
categories: [templates]
type: [sub-nav-item]
title: Events 
permalink: /templates/events/
overview: This spec will cover the event content type and all connected templates. 

content-model:
  - name: Title
    type: text
    content: 80 characters
    required: yes
  - name: Event Type
    type: select list
    content: Virtual | In-person | Hybrid | Calls for Papers
    required: yes
  - name: Sponsor
    type: text
    required: yes
  - name: Website
    type: url
    content: must pass url validation creteria
    required: yes
  - name: Street address
    type: text
    required: yes
  - name: Street address line 2
    type: text
  - name: City
    type: text
    required: yes
  - name: States & Territories
    type: select list
    content: The 50 states + Territories list
    required: yes
  - name: ZIP code
    type: text
    content: limit 10 characters
    required: yes
  - name: Start Date
    type: date
    required: yes
  - name: Start Time
    type: time
    required: yes
  - name: End Date
    type: date
    required: yes
  - name: End Time
    type: time
    required: yes
  - name: Time Zone
    type: select
    content: US time zones
    





---
