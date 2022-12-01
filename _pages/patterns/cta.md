---
layout: pattern
categories: [patterns, card]
title: Find Help CTA
type: [sub-nav-item]
permalink: /patterns/help-cta/
variations: true
description: |
   This layout allows for an image with padding. For this layout use the  ```usa-card__media--inset```  on the media class. The example in the html below shows how to apply. _see more details on functionality on the [default card](/patterns/card) page_
overview: This layout allows for an image with padding.

usa-link:
specification: 
spec:
cards:
  - title: Card 1
    content: card 1 content
    button: Learn more about card 1
    img: https://designsystem.digital.gov/img/introducing-uswds-2-0/built-to-grow--alt.jpg
    alt: placeholder image
    media-class: usa-card__media--inset
  - title: Card 2
    content: card 2 content
    button: Learn more about card 2
    img: https://designsystem.digital.gov/img/introducing-uswds-2-0/built-to-grow--alt.jpg
    alt: placeholder image
    media-class: usa-card__media--inset
  - title: Card 3
    content: card 3 content
    button: Learn more about card 3
    img: https://designsystem.digital.gov/img/introducing-uswds-2-0/built-to-grow--alt.jpg
    alt: placeholder image
    media-class: usa-card__media--inset
yml: |
  
  cards:
  - title: Card 1
    content: card 1 content
    button: Learn more about card 1
    img: https://designsystem.digital.gov/img/introducing-uswds-2-0/built-to-grow--alt.jpg
    alt: placeholder image
    media-class: usa-card__media--inset

jekyll: |

  "{% include patterns/card/card-cta-help-jk.md %}"
### Paths to view design and code... 
## designimg: can be used to show an image of the design until a coded version can be created. The htmlpath & csspath should be located in the pattens folder. Read more about creating coded components in /docs/creating-patterns 
# designimg: 
htmlpath: patterns/card/card-cta-report.md
csspath: patterns/card/index.scss
---