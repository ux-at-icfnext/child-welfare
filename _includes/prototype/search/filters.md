<div class="search-filters-sm">
  <div class="filter-controls-sm grid-row">
  <div class="usa-accordion mobile-filter grid-col-5">
    <h4 class="usa-accordion__heading">
      <button
        class="usa-accordion__button"
        aria-expanded="false"
        aria-controls="m1"
      >
        Filter Your Results
      </button>
    </h4>
    <div id="m1" class="usa-accordion__content usa-prose">
      {% include prototype/search/filter-accordions-sm.md %}
    </div>
  </div>
  </div>
  <div class="grid-col-7">
    {% include prototype/search/filter-display.md %}
  </div>
</div>

<div class="search-filters-lg">
  <div class="filter-controls grid-row">
    <div class="grid-col-6"><h4>Filter Your Results</h4></div>
    <div class="grid-col-6"><a href="/" class="usa-button usa-button--outline">Clear Filters</a></div>
  </div>
  <div>
    {% include prototype/search/filter-accordions.md %}
  </div>
</div>


