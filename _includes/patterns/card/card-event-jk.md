<!-- 
 pass in data using these values
 - event_type
 - title
 - sponsor
 - start_date
-->

<ul class="usa-card-group">
  {% for card in include.content %}
    {% if card.event_type == "hybrid" %}
      { assign type="<i class="fa-thin fa-compass"></i>Hybrid" }
    {% elseif card.event_type == "virtual" %}
      { assign type="<i class="fa-thin fa-video"></i>Virtual" }
    {% elseif card.event_type == "call for papers" %}
      { assign type="<i class="fa-kit fa-campaign"></i>Call for Papers" }
    {% else %}
      { assign type="<i class="fa-this fa-location-dot"></i>In Person" }
    {% endif %}
  <li class="usa-card tablet:grid-col-4">
    <div class="usa-card__container event-card card-default">
    <span class="event_format">{{ type }}</span>
      <div class="usa-card__header">
        <h2 class="usa-card__heading">card.title</h2>
      </div>
      <div class="usa-card__body">
        <p>
          {{ card.start_date | date: "%a, %B %d, %Y, %-I:%M %p" }}
        </p>
      </div>
      <div class="usa-card__footer">
        <p class="sponsor">{{ card.sponsor }} </p>
      </div>
    </div>
  </li>
  {% endfor %}
</ul>