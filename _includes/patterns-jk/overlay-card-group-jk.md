{% assign headings=include.headings %}
{% assign items=include.content %}
{% assign set=include.settings %}
<div class="grid-container">
  <div class="card-group__header" style="display: grid; grid-template-columns: auto auto;">
    {% if headings.title %}<h2>{{ headings.title }}</h2>{% endif %}
    {% if headings.link %}
    <div class="card-group-morelink" style="margin-top: 1rem; justify-self: end;"><a href="{{ headings.link }}">{{ headings.link_text }}</a></div>
    {% endif %}
  </div>
    <div class="">
      <ul>
        <li class="usa-card {{ grid | default:'tablet:grid-col-4'}}">
          <div class="{{ class | default: 'usa-card__container card-default' }}">
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
          <div class="usa-card__footer" style="padding: 0;">
            <a href="{{ card.link }}" class="usa-button" style="display: none;">{{ card.link_text }}</a>
          </div>
        </div>
      </li>
      </ul>
    </div>
  </div>