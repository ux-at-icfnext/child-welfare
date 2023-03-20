---
layout: pattern
categories: [patterns, pullquote]
title: Pullquote
type: [sub-nav-item]
permalink: /patterns/pullquote/
overview: 
description: |
  
    
usa-link: 
specification: |
  
spec:
  - name: title
    class:
    required: true
    type: h3
    content: 80 characters
    example: "Cats are really cool dudes"
  - name: body
    class: usa-classname
    type: text
    required: true
    character: 140 characters
    example: "Run off table persian cat jump eat fish hack. Paw at beetle and eat it before it gets away demand"

### Paths to view design and code... 
## designimg: can be used to show an image of the design until a coded version can be created. The htmlpath & csspath should be located in the pattens folder. Read more about creating coded components in /docs/creating-patterns 
# designimg: 

paragraph-class:
### additional style for paragraph element
li-class:
### additional style for process list item 
h4-class:
### additional style for h4 element

  
jekyll: |
  "{% include patterns/pullquote/pullquote-jk.md %}"
htmlpath: patterns/pullquote/pullquote.md
csspath: patterns/pullquote/index.scss
---