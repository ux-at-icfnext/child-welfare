---
layout: default
title: Campaign Landing page
categories: [prototype]
type: [sub-nav-item, prototype]
permalink: /prototype/campaign/2
summary: This is example of a campaign page.

hero:
  - title: Campaign Name
    content: "Campaign Subtitle, consisting of a short description of the campaign. This can be two to three lines in length."
    link_text: Get Involved
    media: /assets/icons/images/subscription-banner.png
    alt: placeholder image
    media-class: usa-card__media--inset


story:
  headings:
    title: Explore Topics
    link: "#"
    link_text: "View all Topics"
  lists:
    - title: "First Item Title Link"
      content: "Learn more about working with families to enhance their capacity to care and protect their children."
      media: /assets/icons/images/family-practice.jpg
    - title: Second Item Title Link
      content: "Write short description of third item here. Two lines max."
      media: /assets/icons/images/500_F_306140481.jpg
    - title: Third Item Title Link
      content: "Write short description of third item here. Two lines max."
      media: /assets/icons/images/medical.jpg
    - title: Fourth Item Title Link
      content: "Write short description of third item here. Two lines max."
      media: /assets/icons/images/1000_F_135780146.jpeg
      
resource:
  headings: 
    title: Resources
  settings:
    group_class: "card-default"
  lists: 
    - title: Title One Goes Here
      content: Ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque.
      media: https://placekitten.com/200/139
      campaign-class: usa-card__container__campaign-one
    - title: Title Two Goes Here
      content: Ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque.
      media: https://placekitten.com/200/139
      campaign-class: usa-card__container__campaign-two
    - title: Title Three Goes Here
      content: Ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque.
      media: https://placekitten.com/200/139
      campaign-class: usa-card__container__campaign-three



---
<style>
  .usa-hero{
    margin-bottom: 0;
  }
</style>

<section class="campaign-hero-section">
  {% include patterns/hero/hero-full-width-campaign-jk.md content=page.hero %}
</section>
<section class="campaign-impact-section">
  {% include prototype/campaign/impact_pie.md %}
</section>
<section class="campaign-news" style="margin-top: 75px;">
{% include patterns-jk/card-flag-group-jk.md headings=page.story.headings content=page.story.lists %}
</section>

{% include prototype/campaign/involved_vision.md %}

<section class="blue-wrapper campaign-resources">
{% include patterns-jk/card-group-campaign.md headings=page.resource.headings content=page.resource.lists settings=page.resource.settings %}
</section>