<div class="{{ page.cards.class | default: 'gray-wrapper' }}">
  <ul class="usa-card-group">
    {% for card in page.cards.schema %}
      <li class="{{ page.cards.columns | default: 'tablet:grid-col-4'}} usa-card usa-card--title-only">
        <a href="{{ card.link }}">
        <div class="usa-card__container">
          <div class="usa-card__body">
            <h4>{{ card.card-title}}</h4>
          </div>
        </div>
          </a>
      </li>
    {% endfor %}
  </ul>
</div>