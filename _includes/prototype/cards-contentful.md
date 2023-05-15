{% assign set=include.settings %}

{% if set.grid_class %}
    {% assign grid=set.grid_class %}
{% endif %}
{% if set.group_class %}
    {% assign class=set.group_class %}
{% endif %}

 {% for card in include.content %}
 <li class="tablet:grid-col-4 usa-card">
  <div class="{{ class | default: 'usa-card__container card-default'}}">
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
      <h3 class="usa-card__heading" style="font-family: 'Montserrat';">{{ card.title }}</h3>
    </header>
    {% endif %}
    {% if card.summary %}
    <div class="usa-card__body" style="padding-bottom: 1.5rem;">
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