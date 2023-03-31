<div class="event-sponsor-logo">
  <div><img src="{{ page.logo.url }}" alt="sponsor logo"></div>
  <div><a href="#" class="usa-button secondary__button">Visit {{ page.sponsor }} Website</a></div>
</div>

<div class="event-sponsor">
  <h2>Sponsor</h2>
  <p>{{ page.sponsor }}</p>
</div>

<div class="event-date">
  <h2>Date and time</h2>
  <div>{{ page.start_date | date: "%a, %B %d, %Y, %-I:%M %p"}} - </div>
  <div>{{ page.end_date | date: "%a, %B, %d, %Y, %-I:%M %p" }} <span class="timezone">{{ page.time_zone }}</span></div>
</div>

<div class="event-address">
  <h2>Location</h2>
  <div class="usa-tag">(icon) event type -- needs if/then</div> 
  <p>{{ page.street_address }}</p>
  {% if street_address_2 %}
    <p>{{ page.street_address2 }}</p>
  {% endif %}
  <p>{{ page.city }}, {{ page.state }}, {{ page.zip }}</p>
</div>

<div class="event-cost">
  <h2>Cost</h2>
  <p> {{ page.cost }}</p>
</div>

{% if page.continuing_education %}
<div class="event-education">
  <h2>Continuing Education Units</h2>
  <p> Yes</p>
</div>
{% endif %}

