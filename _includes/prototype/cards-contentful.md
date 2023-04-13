 {% for card in include.content %}
 <li class="tablet:grid-col-4 usa-card">
  <div class="usa-card__container__media">
  {% if card.thumbnail %}
    <div class="usa-card__media">
      <div class="usa-card__img">
        <img
          src="{{ card.thumbnail.url }}"
          alt="{{ card.thumbnail.description }}"
        />
      </div>
    </div>
    {% endif %}
    {% if card.title %}
    <header class="usa-card__header">
      <h3 class="usa-card__heading">{{ card.title }}</h3>
    </header>
    {% endif %}
    {% if card.summary %}
    <div class="usa-card__body">
      <p>{{ card.summary | truncate: 140}}</p>
    </div>
    {% endif %}
    {% if card.link_text %}
    <footer>
      <a href="{{card.link}}" class="usa-button secondary__button" alt="Read more about {{ card.title }}">{{ card.link_text | default:"Read more"}}</a>
    </footer>
    {% endif %}
  </div>
</li>
{% endfor %}