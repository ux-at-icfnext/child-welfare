<div class="event-sponsor">
  <div><img src="{{ page.logo.url }}" alt="sponsor logo"></div>
  <div><a href="#" class="usa-button secondary__button">Visit {{ page.sponsor }} Website</a></div>
</div>

<h2>Sponsor</h2>
<p>{{ page.sponsor }}</p>

<h2>Date and time</h2>
<div>{{ page.state_date }} - </div>
<div>{{ page.end_date }} <span class="timezone">{{ page.time_zone }}</span></div>

<h2>Location</h2>
<div class="usa-tag">(icon) event type -- needs if/then</div>
<div class="event-address">
  <p>{{ page.street_address }}</p>
  TODO: Double check street address 2 variable
  {% if street_address_2 %}
    <p>{{ page.street_address_2 }}</p>
  {% endif %}
  <p>{{ page.city }}, {{ page.state }}, {{ page.zip }}</p>
  