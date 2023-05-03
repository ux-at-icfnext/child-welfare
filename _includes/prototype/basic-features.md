<div class="blue-wrapper">
  <div class="grid-container">
    <ul class="usa-card-group">
    {% for card in page.features %}
      <li class="tablet:grid-col-4 usa-card">
        <div class="card-default card-features">
          <header class="usa-card__header">
            <h3 class="usa-card__heading">{{ card.title}}</h3>
          </header>
          <div class="usa-card__body">
            <p>{{ card.body }}</p>
          </div>
          <footer>
            <a href="{{card.link}}" class="usa-button secondary__button" style="margin-top: 1.5rem;">{{card.button_text}}</a>
          </footer>
      </li>
    {% endfor %}
  </ul>
  </div>
</div>