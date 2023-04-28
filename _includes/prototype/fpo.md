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
                aria-expanded="false"
                aria-controls="b{{forloop.index}}">
                    {{item.title}}
                </button>
            </h4>
            <div id="b{{forloop.index}}" class="usa-accordion__content usa-prose">
              {%for entry in item.list}
                {% assign value = entry.lev | downcase | replace: ' ', '-' %}
                <div class="usa-checkbox">
                    <input class="usa-checkbox__input"
                    id="check-{{value}}"
                    type="checkbox"
                    name="{{category}}"
                    value="{{value}}"
                    />
                    <label class="usa-checkbox__label" for="check-{{value}}">
                        {{entry.lev}}
                    </label>
                </div>
              {% endfor %}
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
    <br>
    <label for="start">End date:</label>
    <input type="date" id="end" name="date-end"
          value="2023-04-28"
          min="1960-04-28" max="2023-04-28">
  </div>
  <h4 class="usa-accordion__heading">
    <button
      class="usa-accordion__button"
      aria-expanded="false"
      aria-controls="a3"
    >
      Foundational Areas
    </button>
  </h4>
  <div id="a3" class="usa-accordion__content usa-prose">
    <div class="usa-accordion accordion">
        {% for item in site.data.filters.Foundational_Areas %}
            <h4 class="usa-accordion__heading">
                <button            
                class="usa-accordion__button"
                aria-expanded="false"
                aria-controls="d{{forloop.index}}">
                    {{item.title}}
                </button>
            </h4>
            <div id="d{{forloop.index}}" class="usa-accordion__content usa-prose">
              {%for entry in item.list}
                {% assign value = entry.lev | downcase | replace: ' ', '-' %}
                <div class="usa-checkbox">
                    <input class="usa-checkbox__input"
                    id="check-{{value}}"
                    type="checkbox"
                    name="{{category}}"
                    value="{{value}}"
                    />
                    <label class="usa-checkbox__label" for="check-{{value}}">
                        {{entry.lev}}
                    </label>
                </div>
              {% endfor %}
            </div>
        {%endfor%}
    </div>
  </div>
  <h4 class="usa-accordion__heading">
    <button
      class="usa-accordion__button"
      aria-expanded="false"
      aria-controls="a4"
    >
      Program Funding
    </button>
  </h4>
  <div id="a4" class="usa-accordion__content usa-prose">
    {% for item in site.data.filters.Program_Funding %}
      {% assign value = item.title | downcase | replace: ' ', '-' %}
      <div class="usa-checkbox">
          <input class="usa-checkbox__input"
          id="check-{{value}}"
          type="checkbox"
          name="{{category}}"
          value="{{value}}"
          />
          <label class="usa-checkbox__label" for="check-{{value}}">
              {{item.title}}
          </label>
      </div>
    {% endfor %}
  </div>
  <h4 class="usa-accordion__heading">
    <button
      class="usa-accordion__button"
      aria-expanded="false"
      aria-controls="a5"
    >
      Resources For
    </button>
  </h4>
  <div id="a5" class="usa-accordion__content usa-prose">
    {% for item in site.data.filters.Resources_For %}
      {% assign value = item.title | downcase | replace: ' ', '-' %}
      <div class="usa-checkbox">
          <input class="usa-checkbox__input"
          id="check-{{value}}"
          type="checkbox"
          name="{{category}}"
          value="{{value}}"
          />
          <label class="usa-checkbox__label" for="check-{{value}}">
              {{item.title}}
          </label>
      </div>
    {% endfor %}
  </div>
  <h4 class="usa-accordion__heading">
    <button
      class="usa-accordion__button"
      aria-expanded="false"
      aria-controls="a6"
    >
      Format
    </button>
  </h4>
  <div id="a6" class="usa-accordion__content usa-prose">
    {% for item in site.data.filters.Format %}
      {% assign value = item.title | downcase | replace: ' ', '-' %}
      <div class="usa-checkbox">
          <input class="usa-checkbox__input"
          id="check-{{value}}"
          type="checkbox"
          name="{{category}}"
          value="{{value}}"
          />
          <label class="usa-checkbox__label" for="check-{{value}}">
              {{item.title}}
          </label>
      </div>
    {% endfor %}
  </div>
  <h4 class="usa-accordion__heading">
    <button
      class="usa-accordion__button"
      aria-expanded="false"
      aria-controls="a7"
    >
      Resource Type
    </button>
  </h4>
  <div id="a7" class="usa-accordion__content usa-prose">
    {% for item in site.data.filters.Resource_Type %}
      {% assign value = item.title | downcase | replace: ' ', '-' %}
      <div class="usa-checkbox">
          <input class="usa-checkbox__input"
          id="check-{{value}}"
          type="checkbox"
          name="{{category}}"
          value="{{value}}"
          />
          <label class="usa-checkbox__label" for="check-{{value}}">
              {{item.title}}
          </label>
      </div>
    {% endfor %}
  </div>
  <h4 class="usa-accordion__heading">
    <button
      class="usa-accordion__button"
      aria-expanded="false"
      aria-controls="a8"
    >
      Authhor/ Source
    </button>
  </h4>
  <div id="a8" class="usa-accordion__content usa-prose">
    {% for item in site.data.filters.Author_Source %}
      {% assign value = item.title | downcase | replace: ' ', '-' %}
      <div class="usa-checkbox">
          <input class="usa-checkbox__input"
          id="check-{{value}}"
          type="checkbox"
          name="{{category}}"
          value="{{value}}"
          />
          <label class="usa-checkbox__label" for="check-{{value}}">
              {{item.title}}
          </label>
      </div>
    {% endfor %}
  </div>
  <h4 class="usa-accordion__heading">
    <button
      class="usa-accordion__button"
      aria-expanded="false"
      aria-controls="a9"
    >
      Language
    </button>
  </h4>
  <div id="a9" class="usa-accordion__content usa-prose">
    Toggle
  </div>
  <h4 class="usa-accordion__heading">
    <button
      class="usa-accordion__button"
      aria-expanded="true"
      aria-controls="a10"
    >
      States, Territories, and Tribes
    </button>
  </h4>
  <div id="a10" class="usa-accordion__content usa-prose">
    <div class="usa-accordion accordion">
        {% for item in site.data.filters.States_Territories_Tribes %}
            <h4 class="usa-accordion__heading">
                <button            
                class="usa-accordion__button"
                aria-expanded="false"
                aria-controls="g{{forloop.index}}">
                    {{item.title}}
                </button>
            </h4>
            <div id="g{{forloop.index}}" class="usa-accordion__content usa-prose">
              {%for entry in item.list}
                {% assign value = entry.lev | downcase | replace: ' ', '-' %}
                <div class="usa-checkbox">
                    <input class="usa-checkbox__input"
                    id="check-{{value}}"
                    type="checkbox"
                    name="{{category}}"
                    value="{{value}}"
                    />
                    <label class="usa-checkbox__label" for="check-{{value}}">
                        {{entry.lev}}
                    </label>
                </div>
              {% endfor %}
            </div>
        {%endfor%}
    </div>
  </div>
</div>

