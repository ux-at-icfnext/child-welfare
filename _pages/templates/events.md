---
layout: left-rail
categories: [templates, events]
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
  - name: Logo
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
    content: this is used for both Eligibility and Who should attend
  - name: Summary
    type: rich text
    content: 250 words - allows bullets, heading levels h3 through h6, links
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
  - name: Email
    type: email
    content: must pass email format validation
    required: yes
 
  



---
Events and Call for Papers allow Organization to add their activities to the Childwelfare site. There are font-end facing forms which allow these organizations to add. There will need to be an internal author review before content is published to the site. Additionally, internal authors will need to be able to create CWIG sponsored activites. 

These experiences all use the Event content type:
- [Event Landing](/templates/events/landing)
- [Event Search](/templates/search-event)
- [Event Detail](/templates/events/detail)
- [Call for Papers Detail](/templates/events/papers)
- [Add Event / Call for Papers Form](/templates/events/form)

## Event Content Model
<table class="usa-table">
    <thead>
        <tr>
            <td>Name</td>
            <td>Type</td>
            <td>Required?</td>
            <td>Content Specifications</td>
            <td>Error</td>
        </tr>
    </thead>
    {% for spec in page.content-model %}
    <tbody>
        <tr>
            <td>{{ spec.name }} </td>
            <td>{{ spec.type }}</td>
            <td>{{ spec.required }}</td>
            <td>{{ spec.content }}</td>
            <td>{{ spec.error }}</td>
        </tr>
    </tbody>
    {% endfor %}
</table>