<div class="grid-container">
<div class="usa-accordion usa-tabs">
    {% for item in page.list %}
        <h4 class="usa-accordion__heading">
            <button
            class="usa-accordion__button"
            {% if item.title == "Overview"%}
            aria-expanded="true"
            {%endif%}
            aria-expanded="false"
            aria-controls="a{{forloop.index}}"
            >
                {{ item.title }}
            </button>
        </h4>
        <div id="a{{forloop.index}}" class="usa-accordion__content usa-prose">
            {% if item.content_title %}
            <h3>{{item.content_title}}</h3>
            {% endif %}
            <p>
                {{ item.content | markdownify }}
            </p>
        </div>
    {% endfor %}
</div>

</div>

