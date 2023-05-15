<div class="usa-accordion accordion">
    {% for i in (1..4) %}
        <h4 class="usa-accordion__heading">
            <button
            class="usa-accordion__button"
            aria-expanded="false"
            aria-controls="a{{forloop.index}}"
            >
                190{{forloop.index}}
            </button>
        </h4>
        <div id="a{{forloop.index}}" class="usa-accordion__content usa-prose">
            {% include prototype/timeline/card.md %}
        </div>
    {% endfor %}
</div>