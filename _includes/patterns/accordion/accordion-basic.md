<div class="usa-accordion accordion">
    {% for item in page.list %}
        <h4 class="usa-accordion__heading">
            <button
            class="usa-accordion__button"
            aria-expanded="false"
            aria-controls="a{{forloop.index}}"
            >
                {{ item.title }}
            </button>
        </h4>
        <div id="a{{forloop.index}}" class="usa-accordion__content usa-prose">
            <p>
                {{ item.content | markdownify }}
            </p>
        </div>
    {% endfor %}
</div>