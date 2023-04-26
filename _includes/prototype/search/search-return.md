{% assign page.search="search" %}

<div class="search-functions-group grid-container">
  <div class="grid-row grid-gap-lg" style="margin-top: 2rem;">
    <div class="search-searchbar desktop:grid-col-8" style="padding-top: 0.5rem;">
      {% include patterns/search/search-small.md %}
    </div>
    <div class="search-sort desktop:grid-col-4">
      <div class="usa-combo-box" style="display: inline-flex;"><span class="text-bold" style="padding-right: 0.5rem; padding-top: 1rem;">Sort By</span>
      <select class="usa-select" style="width: 8rem;" name="view" id="view">
        <option value="Relevance">Relevance</option>
        <option value="Latest Published">Latest Published</option>
        <option value="A-Z">A-Z</option>
      </select>
    </div>
    </div>
  </div>
  {% include prototype/search/filter-display.md %}
  <div class="applied-filters" style="margin-bottom: 2rem;" >
    <span class="text-bold">Applied Filters:</span><span class="usa-tag">All Resource Types <i class="fa-kit fa-close"></i></span>
  </div>
  <div class="return-list">
    {% for i in (1..10) %}
    {% include prototype/search/return-list.md %}
    {% endfor %}
  </div>
</div>
