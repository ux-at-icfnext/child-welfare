
{% for hero in include.content" %}
<div class="design-preview">
  <section class="usa-hero full-hero-image" style="background-image: url({{ hero.media }});" aria-label="Introduction">
    <div class="grid-container">
    {% if hero.content %}
    <h1>{{ hero.title }}</h1>
    <div class="intro" style="max-width: 60ex;">{{ hero.content }}</div>
    <a href="{{ hero.link }}" class="usa-button">{{ hero.link_text }}</a>
    {% endif %}
    </div>
  </section>
</div>
{% endfor %}
