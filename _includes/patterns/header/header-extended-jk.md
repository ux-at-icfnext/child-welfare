
<div class="usa-overlay"></div>
<header class="usa-header usa-header--extended">
  <div class="usa-navbar">
    <div class="usa-logo content-flex" id="-logo">
     <img src="/assets/icons/cwig-logo-inverse.svg" width="auto" height="52">
    </div>
    <button class="usa-menu-btn">Menu</button>
  </div>
  <nav aria-label="Primary navigation" class="usa-nav">
    <div class="usa-nav__inner">
      <ul class="usa-nav__primary usa-accordion">
      {% for item in site.data.proto-nav %}
        <li class="usa-nav__primary-item">
          {% if item.subtitle %}
          <button
            class="usa-accordion__button "
            aria-expanded="false"
            aria-controls="extended-nav-section-one{{forloop.index}}"
          >
            <span>{{ item.title }}<i class="fas fa-chevron-down"></i></span>
          </button>
          {% else %}
          <a href="" class="usa-nav-link" style="padding-top: -2px;"><span>{{ item.title }}</span></a>
          {% endif %}
          <ul id="extended-nav-section-one{{forloop.index}}" class="usa-nav__submenu">
          {% for sub in item.subtitle %}
            <li class="usa-nav__submenu-item">
              <a href=""><span class="sub-item">{{ sub }}</span></a>
            </li>
          {% endfor %}
          </ul>
        </li>
        {% endfor %}
      </ul>
      <div class="usa-nav__secondary usa-header--extended">
        <ul class="usa-nav__secondary-links">
          <li><a href="">How to Report Abuse or Neglect</a></li>
          <li><span class="divider">|</span></li>
          <li><a href="">Find Help With a Personal Situation</a></li>
        </ul>
        <section aria-label="Search component">
          <form class="usa-search usa-search--small" role="search">
            <label class="usa-sr-only" for="search-field">Search</label>
            <input
              class="usa-input"
              id="search-field"
              type="search"
              name="search"
              style="border: 0.1px solid white;"
            />
            <button class="usa-button" type="submit">
              <img
                src="/assets/img/usa-icons-bg/search--white.svg"
                class="usa-search__submit-icon"
                alt="Search"
              />
            </button>
          </form>
        </section>
      </div>
    </div>
  </nav>
</header>