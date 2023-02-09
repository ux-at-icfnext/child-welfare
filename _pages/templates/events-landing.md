---
layout: template
categories: [templates, events]
type: [detail-page]
title: Events Landing
permalink: /templates/events/landing
overview: The Event Landing page is the first page in the events browsing journey. 
description: The Event Landing page is the first page in the events browsing journey. Please see the [Events](/templates/events) page for information about the Event content type.

specs:
  - name: Title
    type: h1
    content: "Events"
    authored: yes
    required: yes
    searchable: yes
  - name: Summary
    type: text
    content: 250 words maximum
    required: yes
    authored: yes
  - name: Featured
    type: list
    authored: yes
    content: Author chooses up to 3 events from the event content type. The Title, Start Date & Start Time, Sponsor, and Event type are all stored as a list array.

cards:
  - name: Title
    type: h3
    source: "Event: Title"
  - name: Type
    type: "tag"
    source: "Event: Event Type"
  - name: Date & Time
    type: body-meta
    source: "Event: Start Date & Event: Start Time"
  - name: Sponsor
    type: body
    source: "Event: Sponsor"

prototype:
  - name: Event Landing
    link: https://www.sketch.com/s/dd2f2e71-977c-45b4-baf3-8bf823bfcd0d/p/D13A8BBF-E627-4C8C-83BF-688D149496F5/canvas
---

## Functionality Specifications
This section show the details on how to build the page based on the author selections.

### Page Header
The page header includes the page title (h1), opening summary, and [submission promo](/patterns/summary-box/submissions).
note: _The body has a max-width of 80ex_

**Column Grid large+ screens**
- The Title and summary are 8 columns on the left. 
- The Submissions promo is 4 columns on the right

### Search
OnSubmit of Search button, the system displays the [Event Search](/templates/search-event) page. Note that there is no error state, if the person leaves the form blank, all events show on the result page. Please see that page on more details how the search works.

**Submission form promo**
Uses the [card-event-submission](/patterns/card/card-event-submission).

### Events List
- Uses the [card-event](/patterns/card/card-event)
- Event cards are grouped by 3 -- which line horizontally on large screens and wrap as space condenses until they are virtical on small screens.
- Beneath each event group, there is a link to view the [Event Search](/templates/search-event), with results restricted by the canned link.

<table class="usa-table">
    <thead>
        <tr>
            <td>Name</td>
            <td>Type</td>
            <td>Source</td>
        </tr>
    </thead>
    {% for spec in page.cards %}
    <tbody>
        <tr>
            <td>{{ spec.name }} </td>
            <td>{{ spec.type }}</td>
            <td>{{ spec.source }}</td>
        </tr>
    </tbody>
{% endfor %}
</table>

__Featured__

For the Featured group. Authors are able to choose which items they want to display. So these items should be available through the Event Landing page "Featured" list.

__Upcoming__

Pulls in the Upcoming Events
Canned Link: "See All Upcoming Events" links to the Event Search page... with items sorted by upcoming.

__Information Gateway Events__

Pulls in the Upcoming Events that on are sponsored by Information Gateway
Canned Link: "See All Information Gateway Events" links to the Event Search page... with items sorted by upcoming and filtered to Information Gateway.

__Come See Me At__

Pulls in the Upcoming Events in-person events and conferences by Information Gateway
Canned Link: "See more" links to the Event Search page... with items sorted by upcoming and filtered to Information Gateway.
_note: if there are no events this section is not displayed_



