<style>
  h2{
    line-height: 3rem;
  }
  h3{
    line-height: 2rem;
  }
  .usa-tag{
    width: fit-content;
  }
  .event-tag{
    background-color: #005DAA;
    color: white;
    padding: 5px;
    padding-left: 10px;
    width: fit-content;
    font-weight: bold;
  }
</style>
<div class="event-sponsor-logo">
  <div><img src="{{ page.logo.url }}" alt="sponsor logo"></div>
  <div><a href="#" class="usa-button secondary__button" style="width: 100%;">Visit {{ page.sponsor }} Website</a></div>
</div>

<div class="event-sponsor">
  <h3 style="margin-top: 70px;">Sponsor</h3>
  <p>{{ page.sponsor }}</p>
</div>

<div class="event-date" style="padding-bottom: 25px;">
  <h3>Date and time</h3>
  <div>{{ page.start_date | date: "%a, %B %d, %Y, %-I:%M %p"}} - </div>
  <div>{{ page.end_date | date: "%a, %B, %d, %Y, %-I:%M %p" }} <span class="timezone">{{ page.time_zone }}</span></div>
</div>

<div class="event-address">
  <h3>Location</h3>
  <div class="usa-tag event-tag">
  {% if page.event_type == "hybrid" %}
      <i class="fa-light fa-compass"></i> Hybrid
  {% endif %}
  {% if page.event_type == "virtual" %}
      <i class="fa-light fa-video"></i> Virtual
  {% endif %}
  {% if page.event_type == "in-person" %}
      <i class="fa-light fa-location-dot"></i> In Person
  {% endif %}
  {% if page.event_type == "calls for papers" %}
      <i class="fa-kit fa-campaign"></i> Calls for Papers
  {% endif %}
  
  
  
  </div> 
  <p style="margin-bottom: 0.5rem;">{{ page.street_address }}</p>
  {% if street_address_2 %}
    <p>{{ page.street_address2 }}</p>
  {% endif %}
  <p>{{ page.city }}, {{ page.state }}, {{ page.zip }}</p>
</div>

<div class="event-cost">
  <h3>Cost</h3>
  <p> {{ page.cost }}</p>
</div>

{% if page.continuing_education %}
<div class="event-education">
  <h3>Continuing Education Units</h3>
  <p> Yes</p>
</div>
{% endif %}

