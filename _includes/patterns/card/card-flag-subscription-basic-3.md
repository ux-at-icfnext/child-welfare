<ul class="usa-card-group">
{% for item in site.data.contentful.spaces.example.basic[1].list_groups[2].list %}
  <li class="usa-card usa-card--flag desktop:grid-col-8 usa-card--media-left">
    <div class="usa-card__container__flag-subscribe">
      <div class="usa-card__header">
        <h2 class="usa-card__heading">{{item.title}}</h2>
      </div>
      <div class="usa-card__media usa-card__media--inset">
        <div class="usa-card__img">
          <img
            src="{{item.thumbnail.url}}"
            alt="{{item.thumbnail.description}}"
          />
        </div>
      </div>
      <div class="usa-card__body">
        <p>{{item.body}}</p>
      </div>
      <div class="usa-card__footer">
        <a href="">{{item.link_text}}</a>
      </div>
    </div>
  </li>
  {%endfor%}
</ul>