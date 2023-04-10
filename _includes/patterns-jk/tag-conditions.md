{% if card.tag == "virtual" %}
  <span class="event_format"><i class="fa-thin fa-video"></i>Virtual Event</span>
{% elsif card.tag == "hybrid" %}
  <span class="event_format"><i class="fa-thin fa-compass"></i>Hybrid Event</span>
{% elsif card.tag == "call" %}
<span class="event_format" style="color: white;"><i class="fa-kit fa-campaign" ></i>Call for Papers</span>
{% elsif card.tag == "video" %}
  <span class="event_format"><i class="fa-thin fa-video"></i>Video</span>
{% elsif card.tag == "podcast" %}
  <span class="event_format"><i class="fa-thin fa-podcast"></i>Podcast</span>
{% elsif card.tag == "graphic" %}
  <span class="event_format"><i class="fa-thin fa-image"></i>Graphic</span>
{% elsif card.tag == "webinar" %}
  <span class="event_format"><i class="fa-thin fa-camera-web"></i>Webinar</span>
{% elsif card.tag == "PDF" %}
  <span class="event_format"><i class="fa-thin fa-file-pdf"></i>PDF</span>
{% elsif card.tag == "Publication" %}
  <span class="event_format"><i class="fa-thin fa-book-open-cover"></i>Publication</span>
{% elsif card.tag == "Tool" %}
  <span class="event_format"><i class="fa-thin fa-gear"></i>Tool</span>
{% else %}
  <span class="event_format"><i class="fa-thin fa-location-dot"></i>{{ card.tag }}</span>
{% endif %}