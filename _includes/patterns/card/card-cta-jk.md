<ul class="usa-card-group">
    {% for item in page.cards %}
    <li class="tablet:grid-col-4 usa-card">
        <div class="event__card card-cta">
            <header class="event-card__header">
                <h3>{{item.card-title}}</h3>
            </header>
            <div class="event-card__body">
                <p> {{ item.card-body | default:'Lorem ipsum dolor sit amet consectetur adipisicing elit.'}}</p>
            </div>
             <div class="usa-card__footer">
                <button class="usa-button">{{item.button}}</button>
             </div>
        </div>
    </li>
    {% endfor %}
</ul>