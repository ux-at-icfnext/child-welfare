<div class="resource-attachment-group">
    <div class="publication-info">
      <img src="{{ page.thumbnail.url }}" alt="{{ page.thumbnail.description }}" />
      <div class="resources-body">
          <p><span class="pub-details">Series Title:</span> {{ page.resource.series_title }}</p>
          <p><span class="pub-details">Author(s):</span> {{ page.resource.author }}</p>
          <p><span class="pub-details">Year Published</span> {{ page.resource.year_published }}</p>
          {% if page.title contains "Publication" or page.title contains "PDF" %}
            <span class="download">{%include patterns/button/button-dropdown-resource.md%}</span>
            <span class="download">{%include patterns/button/order-button.md%}</span>
          {% endif %}
          {% if page.title contains "Image" %}
            <span class="download">{%include patterns/button/button-dropdown-image.md%}</span>
            <span class="download">{%include patterns/button/order-button.md%}</span>
          {% endif %}
      </div>
    </div>
    <div class="body-content">
      <p>{{page.body | markdownify}}</p>
    </div>
  </div>