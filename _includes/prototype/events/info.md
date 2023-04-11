<h2>About this Event</h2>
{{ page.summary }}

<h3>Who Should Attend this Conference?</h3>
{{ page.audience }}

<div class="tag-group">
<h3>Topic Tags</h3>
{% for tag in page.tags %}
<div class="usa-tag"> {{ tag }} </div>
{% endfor %}
</div>
<div class="events-related">
  <div class="more-from-sponsor" style="display: grid; grid-template-columns: auto auto;">
    <h2>More from this sponsor</h2>
    <div class="more-link" style="margin-top: 1rem;"><a href="#">See all events from this sponsor</a><i class="fa-kit fa-navigate-next"></i></div>
  </div>


<ul class="usa-card-group">
{% for cards in page.cards %}
  <li class="usa-card tablet:grid-col-5">
    <div class="usa-card__container event-card card-default">
    <span class="event_format"><i class="{{ cards.icon }}"></i> {{ cards.type }}</span>
      <div class="usa-card__header">
        <h2 class="usa-card__heading"> {{ cards.title}}
        </h2>
      </div>
      <div class="usa-card__body">
        <p>
          {{ cards.meta }}
        </p>
      </div>
      <div class="usa-card__footer">
        <p class="sponsor">{{ cards.content }}</p>
      </div>
    </div>
  </li>
  {% endfor %}
</ul>


</div>


{% include patterns/summary-box/summary-box-jk.md %} 
