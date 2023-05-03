<style>
  .sublev{
    padding-left: 2rem;
  }
  /* The switch - the box around the slider */
  .switch {
    position: relative;
    display: inline-block;
    width: 60px;
    height: 34px;
  }

  /* Hide default HTML checkbox */
  .switch input {
    opacity: 0;
    width: 0;
    height: 0;
  }

  /* The slider */
  .slider {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: #ccc;
    -webkit-transition: .4s;
    transition: .4s;
  }

  .slider:before {
    position: absolute;
    content: "";
    height: 20px;
    width: 20px;
    left: 4px;
    bottom: 4px;
    background-color: white;
    -webkit-transition: .4s;
    transition: .4s;
  }

  input:checked + .slider {
    background-color: #2196F3;
  }

  input:focus + .slider {
    box-shadow: 0 0 1px #2196F3;
  }

  input:checked + .slider:before {
    -webkit-transform: translateX(26px);
    -ms-transform: translateX(26px);
    transform: translateX(26px);
  }
  /* Rounded sliders */
.slider.round {
  border-radius: 34px;
}

.slider.round:before {
  border-radius: 50%;
}
</style>

<div class="usa-accordion accordion">
  <h4 class="usa-accordion__heading">
    <button
      class="usa-accordion__button"
      aria-expanded="false"
      aria-controls="g1"
    >
      Topics
    </button>
  </h4>
  <div id="g1" class="usa-accordion__content usa-prose">
    <div class="usa-accordion accordion">
        {% for item in site.data.filters.Topics %}
            <h4 class="usa-accordion__heading">
                <button            
                class="usa-accordion__button"
                aria-expanded="false"
                aria-controls="h{{forloop.index}}">
                    {{item.title}}
                </button>
            </h4>
            <div id="h{{forloop.index}}" class="usa-accordion__content usa-prose">
              {% assign category = item.title | downcase | replace: ' ', '-' %}
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
                <div class="sublev">
                  {% for subentry in entry.sublev %}
                  {% assign value = subentry | downcase | replace: ' ', '-' %}
                  <div class="usa-checkbox">
                      <input class="usa-checkbox__input"
                      id="check-{{value}}"
                      type="checkbox"
                      name="{{category}}"
                      value="{{value}}"
                      />
                      <label class="usa-checkbox__label" for="check-{{value}}">
                          {{subentry}}
                      </label>
                  </div>
                  {%endfor%}
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
      aria-controls="g3"
    >
      Foundational Areas
    </button>
  </h4>
  <div id="g3" class="usa-accordion__content usa-prose">
    <div class="usa-accordion accordion">
        {% for item in site.data.filters.Foundational_Areas %}
            <h4 class="usa-accordion__heading">
                <button            
                class="usa-accordion__button"
                aria-expanded="false"
                aria-controls="i{{forloop.index}}">
                    {{item.title}}
                </button>
            </h4>
            <div id="i{{forloop.index}}" class="usa-accordion__content usa-prose">
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
      aria-controls="g4"
    >
      Program Funding
    </button>
  </h4>
  <div id="g4" class="usa-accordion__content usa-prose">
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
      aria-controls="g5"
    >
      Resources For
    </button>
  </h4>
  <div id="g5" class="usa-accordion__content usa-prose">
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
      aria-controls="g6"
    >
      Format
    </button>
  </h4>
  <div id="g6" class="usa-accordion__content usa-prose">
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
      aria-controls="g7"
    >
      Resource Type
    </button>
  </h4>
  <div id="g7" class="usa-accordion__content usa-prose">
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
      aria-controls="g8"
    >
      Author/ Source
    </button>
  </h4>
  <div id="g8" class="usa-accordion__content usa-prose">
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
      aria-controls="g2"
    >
      Date Range
    </button>
  </h4>
  <div id="g2" class="usa-accordion__content usa-prose">
    <label for="start">Start date:</label>
    <input type="date" id="start" name="date-start"
          value="2023-04-28"
          min="1960-04-28" max="2023-04-28"
          style="margin-bottom: 1rem;">
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
      aria-controls="g9"
    >
      Language
    </button>
  </h4>
  <div id="g9" class="usa-accordion__content usa-prose">
    <span style="vertical-align: bottom; margin-right: 1rem; font-family: 'Montserrat';">Español</span>
    <label class="switch">
    <input type="checkbox">
    <span class="slider round" style="margin-top: 0.5rem;"></span>
</label>
  </div>
  <h4 class="usa-accordion__heading">
    <button
      class="usa-accordion__button"
      aria-expanded="true"
      aria-controls="g10"
    >
      States, Territories, and Tribes
    </button>
  </h4>
  <div id="g10" class="usa-accordion__content usa-prose">
    <div class="usa-accordion accordion">
        {% for item in site.data.filters.States_Territories_Tribes %}
            <h4 class="usa-accordion__heading">
                <button            
                class="usa-accordion__button"
                aria-expanded="false"
                aria-controls="j{{forloop.index}}">
                    {{item.title}}
                </button>
            </h4>
            <div id="j{{forloop.index}}" class="usa-accordion__content usa-prose">
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

