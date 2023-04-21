{% assign page.search="search" %}

<div class="search-functions-group grid-container">
  <div class="grid-row grid-gap-lg">
    <div class="search-searchbar desktop:grid-col-8">
      {% include patterns/search/search-small.md %}
    </div>
    <div class="search-sort desktop:grid-col-4">
      <div class="usa-combo-box"><span class="text-bold">Sort By</span>
      <select class="usa-select" name="view" id="view">
        <option value="Relevance">Relevance</option>
        <option value="Latest Published">Latest Published</option>
        <option value="A-Z">A-Z</option>
      </select>
    </div>
    </div>
  </div>
  {% include prototype/search/filter-display.md %}
  <div class="applied-filters">
    <span class="text-bold">Applied Filters:</span><span class="usa-tag">All Resource Types <i class="fa-kit fa-close"></i></span>
  </div>
  <div class="return-list">
    {% for i in (1..10) %}
    {% include prototype/search/return-list.md %}
    {% endfor %}
  </div>
</div>
