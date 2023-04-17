{% assign headings=include.headings %}
{% assign items=include.content %}
{% assign set=include.settings %}
<div class="grid-container">
  <div class="card-group__header" style="display: grid; grid-template-columns: auto auto;">
    {% if headings.title %}<h2>{{ headings.title }}</h2>{% endif %}
    {% if headings.link %}
    <div class="card-group-morelink" style="margin-top: 1rem; justify-self: end;"><a href="{{ headings.link }}">{{ headings.link_text }}</a></div>
    {% endif %}
  </div>
    <div>
      {% include patterns-jk/card-with-button-jk.md content=items settings=set %}
    </div>
  </div>