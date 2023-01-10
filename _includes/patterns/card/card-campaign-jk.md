<ul class="usa-card-group">
    {% for item in page.cards %}
        <li class="usa-card tablet:grid-col-4">
            <div class="usa-card__container__campaign overlay">
            <div class="usa-card__header">
                <h2 class="usa-card__heading">{{item.heading}}</h2>
            </div>
            <div class="usa-card__body">
                <p>
                {{item.body}}
                </p>
            </div>
            <div class="usa-card__footer">
                <button class="usa-button">{{item.button}}</button>
            </div>
            </div>
        </li>
    {% endfor %}
</ul>