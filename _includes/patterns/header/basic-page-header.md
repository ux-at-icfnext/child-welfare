<section class="usa-hero basic-page-hero" aria-label="Introduction";>
  <div class="grid-container">
    {%include patterns/breadcrumb/breadcrumb-blue-bg.md%}
    <div class="usa-hero__callout basic-page-header">
      <h1 class="usa-hero__heading">
        <span class="usa-hero__heading--alt">{{page.title}}</span>
      </h1> 
      <div>{% include patterns/social-share/social-bar-inverse.md %}</div>
    </div>
    {% if page.find_help_cta %}
      <div class="usa-intro" style="padding-left: 2rem;"> {{page.summary}}</div>
      <div class="help-cards">
        <div class="cta help-cta">
            {%include patterns/card/card-cta-help-heading.md%}
        </div>
        {% if page.child_abuse_cta %}
        <div class="cta report-cta">
            {%include patterns/card/card-cta-report-heading.md%}
        </div>
        {% endif %}
      </div>
    {% endif %}
    {% if page.child_abuse_cta and page.find_help_cta == false %}
      <div class="help-cards">
        <div class="usa-intro"> {{page.summary}}</div>
        <div class="cta report-cta solo-cta">
            {%include patterns/card/card-cta-report-heading.md%}
        </div>
      </div>
    {% endif %}
    {% if page.find_help_cta and page.child_abuse_cta == false %}
      <div class="help-cards">
        <div class="usa-intro"> {{page.summary}}</div>
        <div class="cta help-cta">
            {%include patterns/card/card-cta-help-heading.md%}
        </div>
      </div>
    {% endif %}
  </div>
</section>
