<ul class="usa-card-group {{ page.cards.class | default: 'gray-wrapper' }}">
  {% for card in page.cards.schema %}
    <li class="{{ page.cards.columns | default: 'tablet:grid-col-4'}} usa-card">
      <a href="{{ card.link }}">
      <div class="usa-card__container">
        <header class="usa-card__header">
          <h3 class="usa-card__heading">{{ card.card-title}}</h3>
        </header>
        <div class="usa-card__body">
          <p>{{ card.body }}</p>
        </div>
        </a>
    </li>
  {% endfor %}
</ul>