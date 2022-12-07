---
layout: pattern
categories: [patterns]
title: Search Feature
type: [sub-nav-item]
permalink: /patterns/search-feature/
variations: true
overview: Search allows users to search for specific content if they know what search terms to use or can’t find desired content in the main navigation 
description: Search allows users to search for specific content if they know what search terms to use or can’t find desired content in the main navigation
    
usa-link: "https://designsystem.digital.gov/components/search/"
specification: |
  We will be using the default search component. 
search: Search
### search button text
search-type: 
### search bar type options: big, small
yml: |
  
  search: Search
  ### search button text
  search-type: 
    ### search bar type options: 
        ### big
        ### small
jekyll: |

  "{% include patterns/search/search-feature-jk.md %}"
#spec:

### Paths to view design and code... 
## designimg: can be used to show an image of the design until a coded version can be created. The htmlpath & csspath should be located in the pattens folder. Read more about creating coded components in /docs/creating-patterns 
# designimg: 
htmlpath: patterns/search/search-feature.md
csspath: patterns/search/index.scss
---