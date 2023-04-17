<link href="/assets/css/proto/search.scss" rel="stylesheet">

<div class="search-results grid-container">
  <div class="grid-row">
    <div class="search-filters desktop:grid-col-4">
      {% include prototype/search/filters.md %}
    </div>
    <div class="search-returns desktop:grid-col-8">
      {% include prototype/search/search-return.md %}
    </div>
  </div>
  {% include patterns/pagination/pagination.md %}
</div>
