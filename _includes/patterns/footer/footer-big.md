
<footer class="usa-footer usa-footer--big cwig-footer">
  <div class="grid-container usa-footer__return-to-top">
    <a href="#">Return to top</a>
  </div>
  <div class="footer-quick-exit">
    {% include patterns/button/quick-exit.md %}
  </div>
  <div class="footer-chat-bot">
    {% include patterns/button/chat-bot.md %}
  </div>
  <div class="usa-footer__primary-section">
    <div class="grid-container">
      <div class="grid-row grid-gap">
        <div class="tablet:grid-col-8">
          <nav class="usa-footer__nav" aria-label="Footer navigation,,">
          <div class="grid-row grid-gap-6">
          {% for items in site.data.footer %}
              <div class="mobile-lg:grid-col-6 desktop:grid-col-3">
                <section
                  class="
                    usa-footer__primary-content
                    usa-footer__primary-content--collapsible
                  "
                >
                  <h4 class="usa-footer__primary-link">{{ items.title}} </h4>
                  <ul class="usa-list usa-list--unstyled">
                  {% for sub in items.subtitle %}
                    <li class="usa-footer__secondary-link">
                      <a href="javascript:void(0);"> {{ sub }}</a>
                    </li>
                    {% endfor %}
                  </ul>
                </section>
              </div>
            {% endfor %} 
            </div>
          </nav>
        </div>
      </div>
    </div>
  </div>
  <div class="usa-footer__secondary-section">
    <div class="grid-container">
      <div class="grid-row grid-gap">
        <div
          class="
            usa-footer__logo
            grid-row
            mobile-lg:grid-col-6 mobile-lg:grid-gap-2
            container
          "
        >
          <div class="mobile-lg:grid-col-auto footer-logo">
            <img class="usa-footer__logo-img" src="/assets/icons/cwig-logo-full-color.svg" style="max-width: 100%;" width="auto" height="82" alt="" />
          </div>
        </div>
        <div class="usa-footer__contact-links mobile-lg:grid-col-6">
          <div class="usa-footer__social-links grid-row grid-gap-1">
            <div class="grid-col-auto">
              <a class="usa-social-link" href="javascript:void(0);"
                ><img
                  class="usa-social-link__icon"
                  src="/assets/icons/facebook_footer.svg"
                  alt="Facebook"
              /></a>
            </div>
            <div class="grid-col-auto">
              <a class="usa-social-link" href="javascript:void(0);"
                ><img
                  class="usa-social-link__icon"
                  src="/assets/icons/twitter_footer.svg"
                  alt="Twitter"
              /></a>
            </div>
            <div class="grid-col-auto">
              <a class="usa-social-link" href="javascript:void(0);"
                ><img
                  class="usa-social-link__icon"
                  src="/assets/icons/youtube_footer.svg"
                  alt="YouTube"
              /></a>
            </div>
          </div>
          <address class="usa-footer__address">
            <div class="usa-footer__contact-info grid-row grid-gap">
              <div class="grid-col-auto">
                <a href="tel:1-800-394-3366">1-800-394-3366</a>
              </div>
              <div class="grid-col-auto">
                <a href="mailto:info@childwelfare.gov">info@childwelfare.gov</a>
              </div>
            </div>
          </address>
        </div>
      </div>
    </div>
  </div>
</footer>
