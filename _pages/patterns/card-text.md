---
layout: pattern
categories: [patterns, card]
title: Text Card
type: [detail-page]
permalink: /patterns/card/card-text/
description: |
overview:

usa-link:
cards:
  - title: Card 1
    content: card 1 content
    button: Learn more about card 1
yml: |
  
  cards:
  - title: Card 1
    content: card 1 content
    button: Learn more about card 1

jekyll: |

  "{% include patterns/card/card-text-jk.md %}"
### Paths to view design and code... 
## designimg: can be used to show an image of the design until a coded version can be created. The htmlpath & csspath should be located in the pattens folder. Read more about creating coded components in /docs/creating-patterns 
# designimg: 
htmlpath: patterns/card/card-text.md
csspath: patterns/card/index.scss
---