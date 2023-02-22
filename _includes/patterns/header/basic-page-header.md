<section class="usa-hero" aria-label="Introduction";>
  <div class="grid-container">
    <div class="usa-hero__callout">
      <h1 class="usa-hero__heading">
        <span class="usa-hero__heading--alt">Basic Page</span>
      </h1> 
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
    </div>
    <div class="help-cards">
        {% if page.find-help-cta %}
            {%include patterns/card/card-cta-help-full.md%}
        {% endif %}
        {% if page.child-abuse-cta %}
            personal situation card here
        {% endif %}
    </div>
  </div>
</section>
