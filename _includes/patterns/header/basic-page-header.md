<section class="usa-hero" aria-label="Introduction";>
  <div class="grid-container">
    {%include patterns/breadcrumb/breadcrumb-blue-bg.md%}
    <div class="usa-hero__callout basic-page-header">
      <h1 class="usa-hero__heading">
        <span class="usa-hero__heading--alt">{{page.title}}</span>
      </h1> 
      <div>{% include patterns/social-share/social-share.md %}</div>
      <div class="usa-intro"> {{page.summary}}</div>
    </div>
    <div class="help-cards">
        {% if page.find_help_cta %}
            <div class="cta help-cta">
                {%include patterns/card/card-cta-help-heading.md%}
            </div>
        {% endif %}
        {% if page.child_abuse_cta %}
            <div class="cta report-cta">
                {%include patterns/card/card-cta-report-heading.md%}
            </div>
        {% endif %}
    </div>
  </div>
</section>
