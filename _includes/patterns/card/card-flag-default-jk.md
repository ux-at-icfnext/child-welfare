<ul class="usa-card-group">
  {% for card in page.cards %}
  <li class="usa-card usa-card--flag desktop:grid-col-12 usa-card--media-left">
    <div class="usa-card__container__flag-default">
      <div class="usa-card__header">
        <h2 class="usa-card__heading">{{ card.title }}</h2>
        {% if card.tag %}<p class="card-tag">{{card.tag}}</p>{%endif%}
      </div>
      <div class="usa-card__media usa-card__media--inset">
        <div class="usa-card__img">
          <img style="height: 150px; width: auto;"
            src="{{card.thumbnail.url}}"
            alt="{{card.thumbnail.title}}"
          />
        </div>
      </div>
      <div class="usa-card__body">
        {{card.content}}
      </div>
      {% if card.link_text %}
      <div class="usa-card__footer">
        <a href="{{card.link}}">{{card.link_text}}</a>
      </div>
      {%endif%}
    </div>
  </li>
            
  {% endfor %}
  </ul>