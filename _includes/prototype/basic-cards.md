<div class="grid-container">
  {% for item in page.list_groups %}
  <h2>{{ item.section_heading }}</h2>
  <p>{{ item.section_intro }}</p>
  <ul class="usa-card-group">
  {% for card in item.list %}
  <li class="usa-card usa-card--flag desktop:grid-col-12 usa-card--media-left" style="margin-bottom: 1rem;">
    <div class="usa-card__container__flag-default">
      <div class="usa-card__header">
        <h3 class="usa-card__heading" style="margin-top: 10px; margin-bottom: 10px;">{{ card.title }}</h3>
        <span class="usa-tag">{{card.tag}}</span>
      </div>
      <div class="usa-card__media usa-card__media--inset">
        <div class="usa-card__img">
          <img style="height: 100%; width: 280px;"
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
        <a>{{card.link_text}}</a>
      </div>
      {%endif%}
    </div>
  </li>
            
  {% endfor %}
  </ul>
  {%endfor%}
</div>