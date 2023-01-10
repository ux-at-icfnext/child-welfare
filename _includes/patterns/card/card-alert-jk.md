<ul class="usa-card-group">
    {%for item in page.cards%}
        <li class="usa-card tablet:grid-col-4">
            <div class="usa-card__container__alert">
            <div class="usa-card__header">
                <h2 class="usa-card__heading"><a href="">{{item.heading}}</a></h2>
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
    {%endfor%}
</ul>