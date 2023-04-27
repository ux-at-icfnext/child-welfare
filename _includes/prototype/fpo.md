<div class="usa-accordion accordion">
  <h4 class="usa-accordion__heading">
    <button
      class="usa-accordion__button"
      aria-expanded="true"
      aria-controls="a1"
    >
      Accordion
    </button>
  </h4>
  <div id="a1" class="usa-accordion__content usa-prose">
    <div class="sub-accordion">
        {% for item in page.list.subaccordion %}
            <h4 class="usa-accordion__heading">
                <button button            
                class="usa-accordion__button"
                aria-expanded="false"
                aria-controls="b{{forloop.index}}">
                    {{item.title}}
                </button>
            </h4>
            <div id="b{{forloop.index}}" class="usa-accordion__content usa-prose">
                <form class="usa-form select">
                    <label class="usa-label" for="options">Dropdown label</label>
                    <select class="usa-select" name="options" id="options">
                    <option value>- Select -</option>
                    <option value="value1">Option A</option>
                    <option value="value2">Option B</option>
                    <option value="value3">Option C</option>
                    </select>
                </form>
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
    <div class="date-range" style="display: grid; grid-template-columns: auto auto;">
        <label class="usa-label" for="from">From:</label>
        <div class="usa-combo-box">
        <select class="usa-select" name="from" id="from">
            <option value>Select a year</option>
            <option value="1957">1958</option>
            <option value="1959">1959</option>
            <option value="1960">1960</option>
            <option value="1961">1961</option>
            <option value="1962">1962</option>
            <option value="1963">1963</option>
            <option value="1964">1964</option>
            <option value="1965">1965</option>
            <option value="1966">1966</option>
            <option value="1967">1967</option>
            <option value="1968">1968</option>
            <option value="1969">1969</option>
            <option value="1970">1970</option>
            <option value="1971">1971</option>
            <option value="1972">1972</option>
            <option value="1973">1973</option>
            <option value="1974">1974</option>
            <option value="1975">1975</option>
            <option value="1976">1976</option>
            <option value="1977">1977</option>
            <option value="1978">1978</option>
            <option value="1979">1979</option>
            <option value="1980">1980</option>
            <option value="1981">1981</option>
            <option value="1982">1982</option>
            <option value="1983">1983</option>
            <option value="1984">1984</option>
            <option value="1985">1985</option>
            <option value="1986">1986</option>
            <option value="1987">1987</option>
            <option value="1988">1988</option>
            <option value="1989">1989</option>
            <option value="1990">1990</option>
            <option value="1991">1991</option>
            <option value="1992">1992</option>
            <option value="1993">1993</option>
            <option value="1994">1994</option>
            <option value="1995">1995</option>
            <option value="1996">1996</option>
            <option value="1997">1997</option>
            <option value="1998">1999</option>
            <option value="2000">2000</option>
            <option value="2001">2001</option>
            <option value="2002">2002</option>
            <option value="2003">2003</option>
            <option value="2004">2004</option>
            <option value="2005">2005</option>
            <option value="2006">2006</option>
            <option value="2007">2007</option>
            <option value="2008">2008</option>
            <option value="2009">2009</option>
            <option value="2010">2010</option>
            <option value="2011">2011</option>
            <option value="2012">2012</option>
            <option value="2013">2013</option>
            <option value="2014">2014</option>
            <option value="2015">2015</option>
            <option value="2016">2016</option>
            <option value="2017">2017</option>
            <option value="2018">2018</option>
            <option value="2019">2019</option>
            <option value="2020">2020</option>
            <option value="2021">2021</option>
            <option value="2022">2022</option>
        </select>
        </div>
        <label class="usa-label" for="to">To:</label>
        <div class="usa-combo-box">
        <select class="usa-select" name="to" id="to">
            <option value>Select a year</option>
            <option value="1957">1958</option>
            <option value="1959">1959</option>
            <option value="1960">1960</option>
            <option value="1961">1961</option>
            <option value="1962">1962</option>
            <option value="1963">1963</option>
            <option value="1964">1964</option>
            <option value="1965">1965</option>
            <option value="1966">1966</option>
            <option value="1967">1967</option>
            <option value="1968">1968</option>
            <option value="1969">1969</option>
            <option value="1970">1970</option>
            <option value="1971">1971</option>
            <option value="1972">1972</option>
            <option value="1973">1973</option>
            <option value="1974">1974</option>
            <option value="1975">1975</option>
            <option value="1976">1976</option>
            <option value="1977">1977</option>
            <option value="1978">1978</option>
            <option value="1979">1979</option>
            <option value="1980">1980</option>
            <option value="1981">1981</option>
            <option value="1982">1982</option>
            <option value="1983">1983</option>
            <option value="1984">1984</option>
            <option value="1985">1985</option>
            <option value="1986">1986</option>
            <option value="1987">1987</option>
            <option value="1988">1988</option>
            <option value="1989">1989</option>
            <option value="1990">1990</option>
            <option value="1991">1991</option>
            <option value="1992">1992</option>
            <option value="1993">1993</option>
            <option value="1994">1994</option>
            <option value="1995">1995</option>
            <option value="1996">1996</option>
            <option value="1997">1997</option>
            <option value="1998">1999</option>
            <option value="2000">2000</option>
            <option value="2001">2001</option>
            <option value="2002">2002</option>
            <option value="2003">2003</option>
            <option value="2004">2004</option>
            <option value="2005">2005</option>
            <option value="2006">2006</option>
            <option value="2007">2007</option>
            <option value="2008">2008</option>
            <option value="2009">2009</option>
            <option value="2010">2010</option>
            <option value="2011">2011</option>
            <option value="2012">2012</option>
            <option value="2013">2013</option>
            <option value="2014">2014</option>
            <option value="2015">2015</option>
            <option value="2016">2016</option>
            <option value="2017">2017</option>
            <option value="2018">2018</option>
            <option value="2019">2019</option>
            <option value="2020">2020</option>
            <option value="2021">2021</option>
            <option value="2022">2022</option>
        </select>
        </div>
    </div>
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

