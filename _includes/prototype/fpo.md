<div class="usa-accordion accordion">
  <h4 class="usa-accordion__heading">
    <button
      class="usa-accordion__button"
      aria-expanded="true"
      aria-controls="a1"
    >
      Topics
    </button>
  </h4>
  <div id="a1" class="usa-accordion__content usa-prose">
    <div class="usa-accordion accordion">
        {% for item in site.data.filters.Topics %}
            <h4 class="usa-accordion__heading">
            <button
              class="usa-accordion__button"
              aria-expanded="true"
              aria-controls="a1"
            >
              {{item.title}}
            </button>
            </h4>
            <div id="b{{forloop.index}}" class="usa-accordion__content usa-prose">
              <p>Item Content</p>
            </div>
        {%endfor%}
    </div>
  </div>
  <h4 class="usa-accordion__heading">
    <button
      class="usa-accordion__button"
      aria-expanded="false"
      aria-controls="a2"
    >
      Date Range
    </button>
  </h4>
  <div id="a2" class="usa-accordion__content usa-prose">
    <label for="start">Start date:</label>
    <input type="date" id="start" name="date-start"
          value="2023-04-28"
          min="1960-04-28" max="2023-04-28">
    </input>
    <label for="start">End date:</label>
    <input type="date" id="end" name="date-end"
          value="2023-04-28"
          min="1960-04-28" max="2023-04-28">
    </input>
  </div>
  <h4 class="usa-accordion__heading">
    <button
      class="usa-accordion__button"
      aria-expanded="false"
      aria-controls="a3"
    >
      Dropdown
    </button>
  </h4>
  <div id="a3" class="usa-accordion__content usa-prose">
    {% assign category = page.category | downcase | replace: " ", "-" %}
    <label class="usa-label" for="{{category}}">{{page.label}}</label>
    <div class="usa-combo-box">
    <select class="usa-select" name="{{category}}" id="{{category}}">
        <option value>{{page.label}}</option>
        {% for item in page.list %}
        {% assign value = item.value %}
        <option value="{{value | downcase}}">{{value}}</option>
        {% endfor %}
    </select>
    </div>
  </div>
  <h4 class="usa-accordion__heading">
    <button
      class="usa-accordion__button"
      aria-expanded="false"
      aria-controls="a4"
    >
      Multiselect
    </button>
  </h4>
  <div id="a4" class="usa-accordion__content usa-prose">
    <form class="usa-form">
        <fieldset class="usa-fieldset">
        <legend class="usa-legend">Select any {{page.topic | downcase}}</legend>
        {% assign category = page.topic | downcase | replace: ' ', '-' %}
        {% for item in page.checkbox %}
        {% assign value = item.title | downcase | replace: ' ', '-' %}
        <div class="usa-checkbox">
            <input
                {% if item.description %}
                class="usa-checkbox__input usa-checkbox__input--tile"
            {% else %}
                class="usa-checkbox__input"
            {% endif %}
            id="check-{{value}}"
            type="checkbox"
            name="{{category}}"
            value="{{value}}"
            {% if item.disabled %}
                disabled="disabled"
            {% endif %}
            />
            <label class="usa-checkbox__label" for="check-{{value}}">
                {{item.title}}
                {% if item.description %}
                    <span class="usa-checkbox__label-description">
                        {{item.description}}
                    </span>
                {% endif %}
            </label>
        </div>
        {% endfor %}
        </fieldset>
    </form>
  </div>
</div>

