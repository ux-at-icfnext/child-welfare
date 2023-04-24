{% if page.search_type == "resources" or page.search_type=="all" %}
<!-- video example -->
<div class="search-return-item">
  <span class="usa-tag"><i class="fa-light fa-video"></i> Video</span>
  <h3><a href="/">Title of a video resource</a></h3>
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vitae nibh tortor. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam eget aliquam ante, ac placerat turpis. Aliquam sagittis, tellus quis pharetra venenatis, tellus enim eu.
  </p>
</div>

<!-- podcast example -->
<div class="search-return-item">
  <span class="usa-tag"><i class="fa-light fa-podcast"></i> Podcast</span>
  <h3><a href="/">Title of a podcast resource</a></h3>
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vitae nibh tortor. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam eget aliquam ante, ac placerat turpis. Aliquam sagittis, tellus quis pharetra venenatis, tellus enim eu.
  </p>
</div>
{% endif %}

{% if page.search_type == "directory" or page.search_type=="all" %}
<!-- directory example -->
<div class="search-return-item">
  <h3 style="margin-bottom: 0;"><a href="/">Organization Title</a></h3>
  <div class="return-item-meta" style="margin-bottom: 0.5rem;">
    Email: <a href="/">info@organization.com</a> • <a href="/">Contact Form</a> • 123 Sesame Street, New York NY 10001 <br />
    Phone: <a href="/">(555) 555-5555</a> • Toll-free: <a href="/">(800) 555-5555</a> • Fax: <a href="/">(554) 555-5555</a>
  </div>
  <p style="margin-bottom: 1rem;">
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vitae nibh tortor. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam eget aliquam ante, ac placerat turpis. Aliquam sagittis, tellus quis pharetra venenatis, tellus enim eu.
  </p>
  <p style="margin-bottom: 0.5rem;"><span class="text-bold">Primary Function(s):</span> Does this function and that functon</p>
  <div class="org-shares" style="margin-bottom: 2.5rem;">
    <i class="fa-brands fa-square-facebook"></i>
    <i class="fa-brands fa-square-twitter"></i>
    <i class="fa-brands fa-square-youtube"></i>
  </div>
</div>
{% endif %}

{% if page.search_type == "events" or page.search_type=="all" %}
<!-- event example -->
<div class="search-return-item">
  <span class="usa-tag"><i class="fa-light fa-compass"></i> Hybrid Event</span>
  <p class="event-meta">Fri, Jan 24, 2023 | 11 AM PST</p>
  <h3><a href="/">Title of an event</a></h3>
  <p class="event-org">Organization Title</p>
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vitae nibh tortor. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam eget aliquam ante, ac placerat turpis. Aliquam sagittis, tellus quis pharetra venenatis, tellus enim eu.
  </p>
</div>
{% endif %}
