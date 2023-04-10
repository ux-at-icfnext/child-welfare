{% assign headings=include.headings %}
{% assign items=include.content %}
{% assign set=include.settings %}
<div class="grid-container">
    <h2>{{ headings.title }}</h2>
    {% if headings.link %}
    <div class="card-group-morelink"><a href="{{ headings.link }}">{{ headings.link_text }}</a></div>
    {% endif %}
    <div class="">
      {% include patterns-jk/card-jk.md content=items settings=set %}
    </div>
  </div>