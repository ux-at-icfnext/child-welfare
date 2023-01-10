<ul class="usa-card-group">
    {% for item in page.cards %}
        <li class="usa-card tablet:grid-col-4">
            <div class="callout__container__inv">
                <div class="callout__heading">
                    <img class="blue-icon" src="/assets/icons/flag-navy.svg">
                    <img class="white-icon" src="/assets/icons/flag-white.svg">
                </div>
                <div class="callout__inv__body">
                    <h4>{{item.heading}}</h4>
                    <p>{{item.body}}</p>
                </div>
            </div>
        </li>
    {%endfor%}
</ul>