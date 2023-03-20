<div class="usa-accordion usa-tabs">
    {% for item in site.data.contentful.spaces.example.basic[0].list %}
        <h4 class="usa-accordion__heading">
            <button
            class="usa-accordion__button"
            aria-expanded="false"
            aria-controls="t{{forloop.index}}"
            >
                {{ item.title }}
            </button>
        </h4>
        <div id="t{{forloop.index}}" class="usa-accordion__content usa-prose">
            <p>
                {{item.content}}
            </p>
        </div>
    {% endfor %}
</div>