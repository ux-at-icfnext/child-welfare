<ul class="usa-card-group {{ page.cards.class | default: 'blue-wrapper' }}">
  {% for card in include.content %}
  <li class="usa-card tablet:grid-col-4">
    <div class="usa-card-text__container">
      <div class="usa-card__header">
        <a href="/prototype/{{card.slug}}"><h4 class="usa-card-text__heading">{{ card.title}}</h4></a>
      </div>
      <div class="usa-card__body">
          {{ card.summary | truncate: 140 }}
      </div>
    </div>
  </li>
  {% endfor %}
</ul>