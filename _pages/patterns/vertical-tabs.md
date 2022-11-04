---
layout: pattern
categories: [patterns, vertical-tabs]
title: Vertical Tabs
type: [sub-nav-item]
permalink: /patterns/vertical-tabs/
variations: false
overview:  Vertical tabs
description: |
    Vertical tabs

usa-link:
specification: |
    Tab specs
spec:
    - name: heading
      type: plain text
      class: usa-accordion__heading
      required: yes
      content: 80 characters
      example: "First Amendment"
      notes:
    - name: body
      type: plain text
      class: usa-accordion__content
      required: yes
      content: 500 characters
      example: |
        "Congress shall make no law respecting an establishment of religion, or prohibiting the free exercise thereof; or abridging the freedom of speech, or of the press; or the right of the people peaceably to assemble, and to petition the Government for a redress of grievances."
      notes:
    - name: button
      type:  button
      class: usa-accordion__button
      required: yes
      content: 20 characters
      example: "Find out more"
      notes:
accordion:
  - title: Accordion item 1
    content: accordion item 1 content
  - title: Accordion item 2
    content: accordion item 2 content
  - title: Accordion item 3
    content: accordion item 3 content

yml: |
  
  accordion:
  - title: Accordion item 1
    content: accordion item 1 content
  - title: Accordion item 2
    content: accordion item 2 content
  - title: Accordion item 3
    content: accordion item 3 content
jekyll: |

  "{% include patterns/vertical-tabs/vertical-tabs-jk.md %}"

### Paths to view design and code... 
## designimg: can be used to show an image of the design until a coded version can be created. The htmlpath & csspath should be located in the pattens folder. Read more about creating coded components in /docs/creating-patterns 
# designimg: 
htmlpath: patterns/vertical-tabs/vertical-tabs.md
csspath: patterns/vertical-tabs/index.scss
---




