---
layout: template
categories: [templates]
type: [sub-nav-item]
title: Campaign Page
permalink: /templates/campaign
overview: This template is used for campaigns and initiatives.

description: This template is used for campaigns and initiatives. The author has flexibility over the look and feel by choosing different content objects. The prototype shows two possible layouts.

prototype:
  - name: Campaign Example 1
    link: /prototype/campaign/1
  - name: Campaign Example 2
    link: /prototype/campaign/2

alert:
  content: Before developing page layout, please be sure to read about our <a class="usa-link" href="/styles/grids/">Grid System</a>
  type: warning

heros:
  - name: Hero option
    type: hero
    authored: yes
    required: yes
    content: " campaign page hero - choose between: blue, gray or white backround"
    searchable:
    source:
    notes:
  - name: Title
    type: h1
    authored: yes
    required: yes
    content: 80 characters max
    searchable: yes
  - name: Summary
    type: usa-intro
    authored: yes
    required: yes
    content: 250 characters max
    searchable: yes
  - name: Button label
    type: button
    authored: yes
    required: yes
    content: 80 characters max
  - name: Button Link
    type: url
    authored: yes
    required: yes

impact1:
  - name: Title
    type: h1
    authored: yes
    required: yes
    content: 80 characters max
    searchable: yes
  - name: Summary
    type: usa-intro
    authored: yes
    required: yes
    content: 250 characters max
    searchable: yes
  - name: pie chart
    type: infographic
    authored: yes
    required: yes

impact2:
  - name: Title
    type: h1
    authored: yes
    required: yes
    content: 80 characters max
    searchable: yes
  - name: Summary
    type: usa-intro
    authored: yes
    required: yes
    content: 250 characters max
    searchable: yes
  - name: Stats List
    subhead: yes
    type: list
    authored: yes
    required: yes
    content: limit 4
  - name: Stats
    type: number
    authored: yes
    required: yes
  - name: Description
    type: text
    authored: yes
    required: yes
    content: 140 characters max
  
statements:
  - name: Title
    type: h3
    authored: yes
    required: optional
    content: 80 characters max
  - name: Content
    type: text
    authored: yes
    required: yes
    content: 250 characters max
  - name: Button label
    type: button
    authored: yes
    required: optional
    content: 80 characters max
  - name: Button Link
    type: url
    authored: yes
    required: optional

cards3:
  - name: Section Title
    type: h2
    authored: yes
    content: 80 characters max
  - name: List
    subhead: yes
  - name: Title
    type: h3
    authored: yes/dynamic
    required: yes
    content: 80 characters max
    source: "link: title"
  - name: Content
    type: text
    authored: yes/dynamic
    required: yes
    content: 140 characters max
    source: "link: summary"
  - name: Thumbnail
    type: image
    authored: yes/dynamic
    required: yes
    content: image size 300x175
    source: "link: thumbnail"
  - name: Style
    type: toggle
    authored: yes
    content: default | blue transparency
    notes: allows author to use the blue transparency still

cards4:
  - name: Section Title
    type: h2
    authored: yes
    content: 80 characters max
  - name: List
    subhead: yes
  - name: Title
    type: h3
    authored: yes/dynamic
    required: yes
    content: 80 characters max
    source: "link: title"
  - name: Content
    type: text
    authored: yes/dynamic
    required: yes
    content: 140 characters max
    source: "link: summary"
  - name: Thumbnail
    type: image
    authored: yes/dynamic
    required: yes
    content: image size 300x175
    source: "link: thumbnail"

events:
  - name: Section Title
    type: h2
    authored: yes
    content: 80 characters max
  - name: List
    subhead: yes
  - name: Title
    source: "event: title"
  - name: Event Type
    source: "event: event type"
  - name: Location
    source: "event: city, state"
  - name: Date
    source: "event: start date, start time"
  - name: Sponsor
    source: "event: sponsor"

downloads:
  - name: Title
    type: h2
    authored: yes
    required: yes
    content: 80 characters max
  - name: Content
    type: text
    authored: yes
    required: yes
    content: 140 characters max
  - name: File
    type: button
    authored: yes
    required: yes
    content: should be a zip file
  - name: Button Label
    type: label
    authored: yes
    required: yes
    content: 50 characters max

goals:
  - name: Title
    type: h2
    authored: yes
    required: yes
    content: 80 characters max
  - name: Content
    type: text
    authored: yes
    required: yes
    content: 250 characters max
  - name: List
    subhead: yes
  - name: Icon
    type: icon
    authored: yes
    required: yes
    notes: author should be able to choose any USWDS or Fontawesome icon 
  - name: Content
    type: text
    authored: yes
    required: yes
    content: 140 characters max

topicslist:
  - name: Section Title
    type: h2
    notes: Title should either be "Related Resources" or "Related Topics" depending on which type is used
  - name: Type
    type: toggle
    authored: yes
    required: yes
    content: Choose between resource or topic
  - name: List
    subhead: yes
  - name: Title
    source: "link: title"
  - name: URL
    source: "link: destination"

---
## Layout Specifications

{% include patterns/alert/alert-no-icon-jk.md %}

### Page order
The hero needs to be at the top of the page, outside of that, the author should be able to pick the order. This rest the page highlights the content blocks.

### Authoring Items
Most of the content is authored directly on the page... however there are a few patterns where author's have the choice to pull content in dynamically instead. Likely the backend will have to create two blocks in these instances, one to pull content and one for writing. For the patterns that have these options, we've filled out the source filled to show what would be pulled.

#### Hero
Authors can choose between the different hero backgrounds (blue, gray and white)
{% include partials/content-specs.md content=page.heros %}

#### Statements
Statements use a full block navy #002552 bleed behind them with centered white text. The header and button are optional.
{% include partials/content-specs.md content=page.statements %}

#### Impact (with pie chart)
{% include partials/content-specs.md content=page.impact1 %}

#### Impact (with stats)
{% include partials/content-specs.md content=page.impact2 %}


#### 3 up Card Group
Authors should be able to use this pattern to link content dynamically, or author in page. List has limit of 3.
{% include partials/content-specs.md content=page.cards3 %}

#### 4 up Card group
Authors should be able to use this pattern to link content dynamically, or author in page. List has a limit of 4. The first card is displayed as a flag.
{% include partials/content-specs.md content=page.cards4 %}

#### Events
This pattern is dynamic only, the author should choose which events to showcase by taxonomy & date. 

_If the results return 0, the section should automatically collapse. This way author's do not have to come back ad do this manually after a campaign has finished._
{% include partials/content-specs.md content=page.events %}

#### Resources to download
This is for downloading campaign kits. They should be a zip file.
{% include partials/content-specs.md content=page.downloads %}

#### Goals
Limit 8 goals.
{% include partials/content-specs.md content=page.goals %}

#### Related Campaigns Or Topics
This section is completely dynamic, authors can choose the link destinations. Limit 4.
{% include partials/content-specs.md content=page.topicslist %}