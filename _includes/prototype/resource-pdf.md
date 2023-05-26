<div class="resource-group">
    <div class="publication-info grid-row grid-gap-lg">
      <div class="desktop:grid-col-4"> <img src="{{ page.thumbnail.url }}" alt="{{ page.thumbnail.description }}" /></div>
      <div class="resources-body desktop:grid-col-8">
          <p style="margin-bottom: 0.5rem;"><span class="pub-details">Series Title:</span> {{ page.resource.series_title }}</p>
          <p><span class="pub-details">Author(s):</span> {{ page.resource.author }}</p>
          <p><span class="pub-details">Year Published</span> {{ page.resource.year_published }}</p>
          {% if page.resource.download_file_size %}
            <span class="download">{%include patterns/button/button-dropdown-image.md%}</span>
          {% else page.resource.download_language %}
            <span class="download">{%include patterns/button/button-dropdown-resource.md%}</span>
          {% endif %}
          {% if page.resource.order_online %}
            <span class="download">{%include patterns/button/order-button.md%}</span>
          {% endif %}
      </div>
    </div>
    <div class="body-content">
      <p>{{page.body | markdownify}}</p>
    </div>
  </div>
</div>