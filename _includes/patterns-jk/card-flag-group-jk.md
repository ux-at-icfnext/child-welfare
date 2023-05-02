{% assign headings=include.headings %}
{% assign items=include.content %}



<div class="grid-container">
<div class="card-group__header" style="display: grid; grid-template-columns: auto auto;">
  <h2>{{ headings.title }}</h2>
  {% if headings.link %}
  <div class="card-group-morelink" style="margin-top: 1rem; justify-self: end;"><a href="{{ headings.link }}">{{ headings.link_text }} <i class="fa-kit fa-navigate-next" style="margin-left: 10px;"></i></a></div>
  {% endif %}
</div>
  <div class="card-group">
  <!-- show the first item as a flag over the other 3 -->
    <ul class="usa-card-group"> 
      {% for card in items limit: 1 %}
        <li class="usa-card usa-card--flag tablet:grid-col-12">
          <div class="usa-card__container__flag-default">
            {% if card.tag %}
            {% include patterns-jk/tag-conditions.md %}
            {% endif %}
            {% if card.title %}
            <div class="usa-card__header">
              <h2 class="usa-card__heading" style="font-family: Montserrat"><a href="{{ card.link }}">{{card.title}}</a></h2>
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
        </div>
      </li>
      {% endfor %}
    </ul>
<!-- then show the other three as image with media, three up -->
    <ul class="usa-card-group"> 
      {% for card in items offset: 1 %}
        <li class="usa-card tablet:grid-col-4">
          <div class="usa-card__container__media no-hover">
            {% if card.tag %}
            {% include patterns-jk/tag-conditions.md %}
            {% endif %}
            {% if card.media %}
                <div class="usa-card__media card-tripplet">
                    <div class="usa-card__img">
                    <img
                        src="{{card.media}}"
                    />
                    </div>
                </div>
            {% endif %}
          {% if card.title %}
            <div class="usa-card__header">
              <h2 class="usa-card__heading"><a href="{{ card.link }}">{{card.title}}</a></h2>
            </div>
            {% endif %}
          <div class="usa-card__body">
            <p class="card-content">
              {{ card.content }}
            </p>
          </div>
        </div>
      </li>
      {% endfor %}
    </ul>
  </div>
</div>