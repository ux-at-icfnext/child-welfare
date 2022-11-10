<link href='https://fonts.googleapis.com/css?family=Montserrat' rel='stylesheet'>

<div class="resources">
    <ul class="usa-card-group">
        {% for item in page.cards %}
        <li class="tablet:grid-col-4 usa-card">
            <div class="event__card">
                <header class="event-card__header">
                    <span class="event__format">{{item.event-format}}</span>
                    <h3>{{item.event-heading}}</h3>
                </header>
                <div class="event-card__body">
                    <p> {{ item.event-body | default:'Lorem ipsum dolor sit amet consectetur adipisicing elit.'}}</p>
                    <p style="font-weight: bold;">{{item.event-sponsor}}</p>
                </div>
            </div>
        </li>
        {% endfor %}
    </ul>
</div>