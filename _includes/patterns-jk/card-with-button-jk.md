{% assign items=include.content %}
{% assign set=include.settings %}

{% if set.grid_class %}
    {% assign grid=set.grid_class %}
{% endif %}
{% if set.group_class %}
    {% assign class=set.group_class %}
{% endif %}



<ul class="usa-card-group"> 
  {% for card in items %}
    <li class="usa-card {{ grid | default:'tablet:grid-col-4'}}">
      <div class="{{ class | default: 'usa-card__container default-card' }}">
        {% if card.tag %}
        {% include patterns-jk/tag-conditions.md %}
        {% endif %}
        {% if card.title %}
        <div class="usa-card__header">
          <h2 class="usa-card__heading">{{card.title}}</h2>
        </div>
        {% endif %}
        {% if card.media %}
            <div class="usa-card__media">
                <div class="usa-card__img">
                <img
                    src="{{card.media}}"
                />
                </div>
            </div>
        {% endif %}
      <div class="usa-card__body">
        <p class="card-content">
          {{ card.content }}
        </p>
      </div>
      <div class="usa-card__footer">
        <a href="{{ card.link }}" class="usa-button">{{ card.link_text }}</a>
      </div>
    </div>
  </li>
  {% endfor %}
</ul>
