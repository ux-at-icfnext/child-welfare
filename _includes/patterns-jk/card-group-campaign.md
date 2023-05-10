{% assign headings=include.headings %}
{% assign items=include.content %}
{% assign set=include.settings %}

<div class="grid-container">
  <div class="card-group__header" style="display: grid; grid-template-columns: auto auto;">
    {% if headings.title %}<h2>{{ headings.title }}</h2>{% endif %}
    {% if headings.link %}
    <div class="card-group-morelink" style="margin-top: 1rem; justify-self: end;"><a href="{{ headings.link }}">{{ headings.link_text }}<i class="fa-kit fa-navigate-next" style="margin-left: 10px;"></i></a></div>
    {%endif%}
  </div>
    <div class="">
        <ul class="usa-card-group">
          {% for card in items %}
        <li class="usa-card tablet:grid-col-4">
            <div class="{{card.campaign-class}} overlay">
              <div class="usa-card__header">
                  <h2 class="usa-card__heading">{{card.title}}</h2>
              </div>
            </div>
            <div class="campaign-card-text">
              <p>{{card.content}}</p>
            </div>
        </li>
        {%endfor%}
        </ul>
    </div>
  </div>