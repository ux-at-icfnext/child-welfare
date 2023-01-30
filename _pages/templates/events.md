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
    content: Virtual - In-person - Hybrid - Calls for Papers
    required: yes
  - name: Sponsor
    type: text
    required: yes
  - name: Website
    type: url
    content: must pass url validation creteria
    required: yes
  - name: Event Photo
    type: file upload
    content: acceptable formats jpg, png, gif. acceptable size, no more than 300 by 200 pixels
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
    required: yes
  - name: Tags
    type: multi-select list
    content: Inclusive Child Welfare Practice - Permanency - Foster Care - Adoption - Child Abuse & Neglect - Preventing Abuse & Neglect - Casework Practice - Connecting Families with Services - Agency Leadership
    required: yes
  - name: Continuing Education Credits
    type: select
    content: Yes - No
    required: yes
  - name: Audience
    type: text
    required: yes
  - name: Summary
    type: text
    content: 250 words
    required: yes
  - name: First Name
    type: text
    required: yes
  - name: Last Name
    type: text
    required: yes
  - name: Phone number
    type: number
    content: limit 10 characters
    required: yes
  - name: Contact Street address
    type: text
    required: yes
  - name: Contact Street address line 2
    type: text
  - name: Contact City
    type: text
    required: yes
  - name: Contact States & Territories
    type: select list
    content: The 50 states + Territories list
    required: yes
  - name: Contact ZIP code
    type: text
    content: limit 10 characters
    required: yes
  

    







---
