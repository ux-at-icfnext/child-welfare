<section class="usa-hero" aria-label="Introduction";>
  <div class="grid-container">
    {%include patterns/breadcrumb/breadcrumb-blue-bg.md%}
    <div class="usa-hero__callout basic-page-header">
      <h1 class="usa-hero__heading">
        <span class="usa-hero__heading--alt">{{page.title}}</span>
      </h1> 
      {%if page.title == "About"%}
        A service of the Children's Bureau, Administration for Children and Families,
        U.S. Department of Health and Human Services, we provide print and electronic
        publications, websites, databases, and online learning tools for improving child
        welfare.
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
      {%endif%}
    </div>
  </div>
</section>
