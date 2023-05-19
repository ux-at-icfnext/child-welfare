<style>
  p{
    margin-bottom: 40px;
  }
</style>

<h2>About this Event</h2>
<p>{{ page.summary }}</p>

<h3>Who Should Attend this Conference?</h3>
<p>{{ page.audience }}</p>

<div class="tag-group">
<h3>Topic Tags</h3>
{% for tag in page.tags %}
<div class="usa-tag" style="margin-bottom:1rem;"> {{ tag }} </div>
{% endfor %}
</div>
<div class="events-related">
  <div class="more-from-sponsor" style="display: grid; grid-template-columns: auto auto;">
    <h2>More from this sponsor</h2>
    <div class="more-link" style="margin-top: 1rem;"><a href="#" style="margin-right: 0.5rem;">See all events from this sponsor</a><i class="fa-kit fa-navigate-next"></i></div>
  </div>


<ul class="usa-card-group">
{% for cards in page.cards %}
  <li class="usa-card tablet:grid-col-5">
    <div class="usa-card__container event-card card-default" style="margin-left: 0;">
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
