<div class="grid-container campaign-involved">
  <h3>Get Involved</h3>

  <ul class="usa-card-group">
  {% for card in page.cards %}
  <li class="usa-card tablet:grid-col-4">
    <div class="usa-card__container__media">
      <div class="usa-card__media">
        <div class="usa-card__img">
          <img src="https://designsystem.digital.gov/img/introducing-uswds-2-0/built-to-grow--alt.jpg" alt="A placeholder image">
        </div>
      </div>
      <div class="usa-card__header">
        <h2 class="usa-card__heading">{{ card.title }}</h2>
      </div>
      <div class="usa-card__body">
        <p>
          {{ card.content }}
        </p>
      </div>
      <div class="usa-card__footer">
        <a href="#" class="usa-button" alt="Read more about {{ card.title }}">{{ card.link_text }} </a>
      </div>
    </div>
  </li>
  {% endfor %}
</ul>

</div>