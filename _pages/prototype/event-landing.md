---
layout: default
title: Events Landing
categories: [prototype]
type: [sub-nav-item, prototype]
permalink: /prototype/events/landing
overview: Event landing page
summary: Event landing page

body: |
  View conferences and calls for papers related to child abuse and neglect, child welfare, and adoption by month and/or state, or submit your conference. Child Welfare Information Gateway exhibit at many conferences throughout the country to provide free materials to the field.  

summary-title: Submit Events and Calls for Papers
summary-class: submissions
summary-list:
  - item: Submit information on your events. We will then post your submission to this website.
  - item: <a href="/">Fill in a submission form </a>

cards:
  - title: "Another Event"
    meta: "Thu, Nov 18 2021 | 11 AM EST"
    content: "Sesame Place"
    type: In Person
    icon: "fa-light fa-location-dot"
  - title: "Another Event"
    meta: "Thu, Nov 18 2021 | 11 AM EST"
    content: "Sesame Place"
    type: In Person
    icon: "fa-light fa-location-dot"
  - title: "Another Event"
    meta: "Thu, Nov 18 2021 | 11 AM EST"
    content: "Sesame Place"
    type: In Person
    icon: "fa-light fa-location-dot"

---

<div class="grid-container" markdown="1">
# {{ page.title }}

<div class="grid-row grid-gap-lg" markdown="1">
  <div class="grid-col-6"> {{ page.body }} </div>
  <div class="grid-col-6"> {% include patterns/summary-box/summary-box-jk.md %} </div>
</div>
</div>

<div class="event-search-banner">
  <div class="grid-container">
    <h2>Find your next event</h2>
    {% include patterns/search/search-small.md%}
    <a href="/prototype/search/events">See all the events</a>
  </div>
</div>

<div class="event-group gray-wrapper">
    <div class="grid-container">
      <h2>Featured Events</h2>
      <ul class="usa-card-group">
      {% for cards in page.cards %}
        <li class="usa-card tablet:grid-col-4">
          <div class="usa-card__container event-card card-default">
          <span class="event_format"><i class="{{ cards.icon }}"></i> {{ cards.type }}</span>
            <div class="usa-card__header">
              <h2 class="usa-card__heading"> {{ cards.title}}
              </h2>
            </div>
            <div class="usa-card__body">
              <p>
                {{ cards.meta }}
              </p>
            </div>
            <div class="usa-card__footer">
              <p class="sponsor">{{ cards.content }}</p>
            </div>
          </div>
        </li>
      {% endfor %}
      </ul>
    </div>
</div>

<div class="event-group gray-wrapper">
    <div class="grid-container">
      <h2>Upcoming</h2>
      <div class="more-link"><a href="#">See all upcoming events</a><i class="fa-kit fa-navigate-next"></i></div>
      <ul class="usa-card-group">
      {% for cards in page.cards %}
        <li class="usa-card tablet:grid-col-4">
          <div class="usa-card__container event-card card-default">
          <span class="event_format"><i class="{{ cards.icon }}"></i> {{ cards.type }}</span>
            <div class="usa-card__header">
              <h2 class="usa-card__heading"> {{ cards.title}}
              </h2>
            </div>
            <div class="usa-card__body">
              <p>
                {{ cards.meta }}
              </p>
            </div>
            <div class="usa-card__footer">
              <p class="sponsor">{{ cards.content }}</p>
            </div>
          </div>
        </li>
      {% endfor %}
      </ul>
    </div>
</div>

<div class="event-group gray-wrapper">
    <div class="grid-container">
      <h2>Information Gateway Events</h2>
      <div class="more-link"><a href="#">See all Information Gateway events</a><i class="fa-kit fa-navigate-next"></i></div>
      <ul class="usa-card-group">
      {% for cards in page.cards %}
        <li class="usa-card tablet:grid-col-4">
          <div class="usa-card__container event-card card-default">
          <span class="event_format"><i class="{{ cards.icon }}"></i> {{ cards.type }}</span>
            <div class="usa-card__header">
              <h2 class="usa-card__heading"> {{ cards.title}}
              </h2>
            </div>
            <div class="usa-card__body">
              <p>
                {{ cards.meta }}
              </p>
            </div>
            <div class="usa-card__footer">
              <p class="sponsor">{{ cards.content }}</p>
            </div>
          </div>
        </li>
      {% endfor %}
      </ul>
    </div>
</div>

<div class="event-group gray-wrapper">
    <div class="grid-container">
      <h2>Come see us in person</h2>
      <div class="more-link"><a href="#">See more</a><i class="fa-kit fa-navigate-next"></i></div>
      <ul class="usa-card-group">
      {% for cards in page.cards %}
        <li class="usa-card tablet:grid-col-4">
          <div class="usa-card__container event-card card-default">
          <span class="event_format"><i class="{{ cards.icon }}"></i> {{ cards.type }}</span>
            <div class="usa-card__header">
              <h2 class="usa-card__heading"> {{ cards.title}}
              </h2>
            </div>
            <div class="usa-card__body">
              <p>
                {{ cards.meta }}
              </p>
            </div>
            <div class="usa-card__footer">
              <p class="sponsor">{{ cards.content }}</p>
            </div>
          </div>
        </li>
      {% endfor %}
      </ul>
    </div>
</div>