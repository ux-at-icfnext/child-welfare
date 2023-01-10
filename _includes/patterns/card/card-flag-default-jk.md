 <ul class="usa-card-group">
    {%for item in page.cards%}
        <li class="usa-card usa-card--flag desktop:grid-col-8 usa-card--media-left">
            <div class="usa-card__container__flag-default">
            <div class="usa-card__header">
                <h2 class="usa-card__heading">{{item.heading}}</h2>
            </div>
            <div class="usa-card__media usa-card__media--inset">
                <div class="usa-card__img">
                <img
                    src="{{item.img}}"
                    alt="{{item.alt-text}}"
                />
                </div>
            </div>
            <div class="usa-card__body">
                <p>{{item.body}}</p>
            </div>
            <div class="usa-card__footer">
                <button class="usa-button">{{item.button}}</button>
            </div>
            </div>
        </li>
    {%endfor%}
</ul>