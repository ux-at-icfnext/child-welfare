---
layout: pattern
categories: [patterns, site-alert]
title: Site alert with list
type: [detail-page]
permalink: /patterns/site-alert/site-alert-list/
overview: Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Interdum velit euismod in pellentesque. 
description: |
    
usa-link: "https://designsystem.digital.gov/components/site-alert/"
specification: |
#spec:
site-alert-type: list
### options: slim, no-header, no-icon, list
site-alert-color: emergency
### options: emergency, info
site-alert-title: Alert message with list
site-alert-list:
  - text: Alert message, and  <a class="usa-link" href="/">a link</a> 
  - text: Alert message, and  <a class="usa-link" href="/">another link</a> 
yml: |
  
  site-alert-type: list
  ### options: 
    ### slim
    ### no-header
    ### no-icon
    ### list
  site-alert-color: emergency
  ### options: 
    ### emergency
    ### info
  site-alert-title: Alert message with list
  site-alert-list:
  - text: Alert message, and <a class="usa-link" href="/">a link</a>
  - text: Alert message, and  <a class="usa-link" href="/">another link</a>
    

jekyll: |

  "{% include patterns/site-alert/site-alert-jk.md %}"
### Paths to view design and code... 
## designimg: can be used to show an image of the design until a coded version can be created. The htmlpath & csspath should be located in the pattens folder. Read more about creating coded components in /docs/creating-patterns 
# designimg: 
htmlexcerpt: patterns/site-alert/site-alert-list-info.md
htmlpath: patterns/site-alert/site-alert-list.md
csspath: patterns/site-alert/index.scss
---