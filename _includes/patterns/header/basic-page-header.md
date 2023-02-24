<section class="usa-hero" aria-label="Introduction";>
  <div class="grid-container">
    {%include patterns/breadcrumb/breadcrumb-blue-bg.md%}
    <div class="usa-hero__callout basic-page-header">
      <h1 class="usa-hero__heading">
        <span class="usa-hero__heading--alt">Basic Page</span>
      </h1> 
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
    </div>
    <div class="help-cards">
        {% if page.find-help-cta %}
            <div class="cta">
                {%include patterns/card/card-cta-help-heading.md%}
            </div>
        {% endif %}
        {% if page.child-abuse-cta %}
            <div class="cta">
                {%include patterns/card/card-cta-report-heading.md%}
            </div>
        {% endif %}
    </div>
  </div>
</section>
