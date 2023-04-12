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
    media: /assets/icons/images/full-image-hero.jpg
    alt: placeholder image
    media-class: usa-card__media--inset


story:
  headings:
    title: News and Stories
    link: "#"
    link_text: "View all news and stories"
  lists:
    - title: "First Item Title Link"
      content: "Learn more about working with families to enhance their capacity to care and protect their children."
      media: https://placekitten.com/200/139
    - title: Second Item Title Link
      content: "Write short description of third item here. Two lines max."
      media: https://placekitten.com/200/139
    - title: Third Item Title Link
      content: "Write short description of third item here. Two lines max."
      media: https://placekitten.com/200/139
    - title: Fourth Item Title Link
      content: "Write short description of third item here. Two lines max."
      media: https://placekitten.com/200/139
      
resource:
  headings: 
    title: Resources
  settings:
    group_class: "card-default"
  lists: 
    - title: Title One Goes Here
      content: Ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque.
      media: https://placekitten.com/200/139
    - title: Title Two Goes Here
      content: Ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque.
      media: https://placekitten.com/200/139
    - title: Title Three Goes Here
      content: Ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque.
      media: https://placekitten.com/200/139



---
{% include patterns/breadcrumb/breadcrumb-jk.md %}
{% include patterns/hero/hero-full-width-jk.md content=page.hero %}

{% include prototype/campaign/impact_pie.md %}

<section class="campaign-news">
{% include patterns-jk/card-flag-group-jk.md headings=page.story.headings content=page.story.lists %}
</section>

{% include prototype/campaign/involved_vision.md %}

<section class="blue-wrapper campaign-resources">
{% include patterns-jk/card-group-jk.md headings=page.resource.headings content=page.resource.lists settings=page.resource.settings %}
</section>