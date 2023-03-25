---
layout: left-rail
categories: [styles]
title: Grids
type: [sub-nav-item]
permalink: /styles/grids/
---

__Contents__
* TOC
{:toc}

### How it works
The USWDS uses a flexible grid system which is mobile-first, powered by flexbox, and based on the 12-column grid system. Nesting grids is also a capibility. For our site, using this grid system is perfered over measuring widith via pixels. You can read more about how the grid system works on [USWDS](https://designsystem.digital.gov/utilities/layout-grid). This guide covers our layout settings.

### Global grids
There are 3 global grid settings to be aware of:
- __.grid-container__ is used for controlling the width of content elements. This is controlled through `$theme-grid-container-max-width` in settings. We have left that unchanged for our design
- __.usa-banner__ is used to controll the width of the banner. This is controlled through `$theme-banner-max-width`.
- __.usa-header__ is used to controll the width of the header. This is controlled through `$theme-header-max-width`.
- __.usa-footer__ is used to controll the width of the footer. This is controlled through `$theme-footer-max-width`.
- __.usa-identifier__ is used to controll the width of the identifier. This is controlled through `$theme-identifier-max-width`.

For this design the banner, header, footer and identifier have all be set to widescreen (1400px). The grid container is left to the default desktop (1024px).

### Theme settings
Please refer to the [Theme Settings](https://designsystem.digital.gov/documentation/settings) documentation for more information on how to work with the settings file.

To apply our grid customizations the settings file should contain:
{% highlight javascript %}
@use "uswds-core" with(
    $theme-banner-max-width: "widescreen",
    $theme-header-max-width: "widescreen",
    $theme-footer-max-width: "widescreen",
    $theme-identifier-max-width: "widescreen",
    $theme-utility-breakpoints: (
                'card': false,   // 160px
                'card-lg': false,   // 240px
                'mobile': false,   // 320px
                'mobile-lg': true,    // 480px
                'tablet': true,    // 640px
                'tablet-lg': false,   // 880px
                'desktop': true,    // 1024px
                'desktop-lg': false,   // 1200px
                'widescreen': true,   // 1400px
        ),

);
{% endhighlight %}

Notice that we set the widescreen to "true" here and added the utitlies for the header and footer.

## Full bleeds
By nature, both the header and foot have fullwidth bleeds (the background color extends to both edges of the screen).
To create a full bleed for the .grid-container, it should be nested inside another div.

For example:
{% highlight html %}
<div class="blue-wrapper">
  <div class="grid-container">
    (content object)
  </div>
<div>
{% endhighlight %}

There are three bleed classes that were created which are most often used behind card groups:
{% highlight css %}
  // body class styles - used behind card groups
  .gray-wrapper {
      background-color: #EDEFF0;
      padding-top: 20px;
      padding-left: 10px;
      padding-right: 10px;
      padding-bottom: 5px;
      margin: auto;
  }

  .blue-wrapper {
      background-color: #EEF1F9;
      padding-top: 20px;
      padding-left: 10px;
      padding-right: 10px;
      padding-bottom: 5px;
      margin: auto;
  }

  .blank-wrapper {
      padding-top: 20px;
      padding-bottom: 5px;
      margin: auto;
      .usa-card__container {
          border: 1px solid #002552;
      }
  }
{% endhighlight %}

## Responsive
Media queries: Grid breakpoints are based on minimum-width media queries, meaning they apply to that specific width and all greater widths (e.g., `tablet:col-4` applies to tablet, desktop, and widescreen devices but not at mobile-lg or any width below the tablet breakpoint). Refer to [USWDS](https://designsystem.digital.gov/utilities/layout-grid/#additional-functionality-2).

A good example for using this responsive technique is in our many card group layouts. By setting the card group class to `tablet:col-4` the cards will layout 3 cards across for tablet devices and above.

Here is an example for layout out a card group that goes 3 across from table up and also has the blue background bleed.

{% highlight html %}
<div class="blue-wrapper">
    <div class="grid-container">
      <ul class="usa-card-group">
        <li class="tablet:grid-col-4 usa-card">
          (card pattern)
        </li>
      </ul>
    </div>
  </div>
{% endhighlight %}