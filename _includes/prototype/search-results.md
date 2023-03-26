### Still to do
- search results examples will go in this file `_includes/prototype/search-results.md` and be shared across all the pages that have search results
- configuration options should be available to display
  - result pattern types (default, event, directory)
- if time permits, pull results from CMS... otherwise use repeated dummy data

<div class="search-results grid-container">
  <div class="grid-row">
    <div class="search-filters desktop:grid-col-4">
      {% include prototype/search/filters.md %}
    </div>
    <div class="search-returns desktop:grid-col-8">
      {% include prototype/search/search-return.md %}
    </div>
  </div>
</div>