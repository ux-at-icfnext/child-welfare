<section class="usa-hero" aria-label="Introduction";>
  <div class="grid-container">
    <div class="usa-hero__callout">
      {% if hero.callout %}
      <h1 class="usa-hero__heading">
        {% if hero.callout.alt %}
        <span class="usa-hero__heading--alt">Hero Callout</span>
        {% endif %}
        {{ hero.callout.text | default: hero.callout }}
      </h1>
      {% endif %}
       {% if hero.image %} 
    <div class="hero-image"><img src="https://via.placeholder.com/150" /></div>
  {% endif %}
      {{ hero.content | markdownify }}
      {% if hero.button %}
      <a class="usa-button"
        href="{{ hero.button.href | relative_url }}">
        Button
      </a>
      {% endif %}
    </div>
  </div>
</section>