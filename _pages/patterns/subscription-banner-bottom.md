---
layout: pattern
categories: [patterns, subscription-banner]
title: Subscription Banner (Bottom)
type: [detail-page]
permalink: /patterns/subscription-banner/subscription-banner-bottom
variations: true
overview:  
description: 
    
usa-link: "https://designsystem.digital.gov/components/summary-box/"
specification: |
  

spec: # example schema below .. repeat sets for as many fields as you have
  - fieldname: title
    class-name: usa-classname
    required: true
    type: h3
    content: 80 characters
    example: "Cats are really cool dudes"
  - fieldname: body
    class-name: usa-classname
    type: text
    character: 140 characters
    example: "Run off table persian cat jump eat fish hack. Paw at beetle and eat it before it gets away demand"
summary-title: Key information
summary-list:
 - item: If you are under a winter storm warning, <a href="/" class="usa-summary-box__link">find shelter</a> right away. 
 - item: Sign up for <a href="/" class="usa-summary-box__link">your community’s warning system</a>.
 - item: Learn the signs of, and basic treatments for, <a href="/"  class="usa-summary-box__link">frostbite</a> and <a href="/" class="usa-summary-box__link">hypothermia</a>.
 - item: Gather emergency supplies for your <a href="/" class="usa-summary-box__link">home</a> and your <a href="/" class="usa-summary-box__link">car</a>.
yml: |
  
  summary-title: Key information
  summary-list:
    - item: If you are under a winter storm warning, <a href="/" class="usa-summary-box__link">find shelter</a> right away. 
    - item: Sign up for <a href="/" class="usa-summary-box__link">your community’s warning system</a>.
    - item: Learn the signs of, and basic treatments for, <a href="/"  class="usa-summary-box__link">frostbite</a> and <a href="/" class="usa-summary-box__link">hypothermia</a>.
    - item: Gather emergency supplies for your <a href="/" class="usa-summary-box__link">home</a> and your <a href="/" class="usa-summary-box__link">car</a>.

jekyll: |

  "{% include patterns/subscription/subscription-banner-bottom-jk.md %}"
### Paths to view design and code... 
## designimg: can be used to show an image of the design until a coded version can be created. The htmlpath & csspath should be located in the pattens folder. Read more about creating coded components in /docs/creating-patterns 
# designimg: 

htmlpath: patterns/subscription/subscription-banner-bottom.md
csspath: patterns/subscription/index.scss
---