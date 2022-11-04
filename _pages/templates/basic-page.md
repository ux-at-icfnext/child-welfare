---
layout: template
categories: [templates]
type: [sub-nav-item]
title: Basic 
permalink: /templates/basic/
overview: The basic page template is used for information or documentation. 

description: |
  The basic page template is used for information or documentation often as the finial destination page in a user's journey. The template was constucted to allow for some variations which allows flexibility to use for pages such as Contact Us or About. Options include ability to show the background color behind the page header as well as using either vertial tabs or accordions to control content.

details: |
  ### Guidance

  #### When to use the documentation page template
  Detailed information on a specific topic. Use a documentation page if you’re presenting detailed information on a specific topic or theme that has already been contextualized by a landing page. Some topics that can be nicely represented on this type of page include guides or how-tos, technical documentation, and program descriptions — in short, any subject that requires in-depth explanation.

  #### Usability Guidance 
  Use a precise headline. A precise headline quickly communicates your page’s purpose. If the page content is especially complex, you may consider using a subheadline to further clarify its meaning.

  Write concise copy. Favor short sentences (and paragraphs) over longer ones, and use straightforward language, avoiding jargon. Remember, copy blocks don’t need to be long to be comprehensive.

  See component-specific guidance. For guidance on specific components, see the page for the individual components.

specs:
- name: Title
  type: h1
  authored: yes
  required: yes
  content: 80 characters max
  searchable: yes
  source:
  notes: 
- name: Summary
  type: text (usa-intro)
  authored: yes
  required: yes
  content: 250 characters max
  searchable: yes
- name: Body
  type: rich text
  authored: yes
  required: yes
  notes: allows h2, h3, h4, bullets, links, icons
- name: Help CTA
  type: multi-select
  content: uses help cards cta
  authored: "no"
  required: optional
  searchable: "no"
  notes: use a toggle in authoring experience to allow authors to choose
- name: Header background
  type: toggle
  authored: "no"
  required: optional
  notes: allows author to choose blue baground for header area
- name: Template layout
  type: toggle
  authored: yes
  required: "np"
  content: "tabs, accordion"
  notes: CMS only
- name: List
  type: vertical tabs or accordion
  authored: yes
  required: yes
  content: multi-valuded... see table below
  searchable: yes
  notes: CMS should use a list to create

specs2:
  - name: List label
    type: text
    authored: yes
    required: yes
    content: 80 characters max
  - name: Content title
    type: h2
    authored: yes
    required: yes
    content: 80 characters max
  - name: Content 
    type: rich text
    authored: yes
    required: yes
    content:  allows h2, h3, h4, bullets, links, icons


components:
  - title: CTA Help Cards
    overview: Hierarchical, vertical navigation to place at the side of a page.
    link: /patterns/side-navigation/
    htmlpath: patterns/card/card.md
  - title: Accordion
    overview: An accordion is a list of headers that hide or reveal additional content when selected. They are helpful for keeping pages clean and easy to navigate.
    link: /patterns/accordion
    htmlpath: patterns/accordion/accordion.md
  - title: Vertical tabs
    overview: They are helpful for keeping pages clean and easy to navigate.
    link: /patterns/accordion
    htmlpath: patterns/accordion/accordion.md

prototype:
  - name: Basic Page
    link: https://www.sketch.com/s/dd2f2e71-977c-45b4-baf3-8bf823bfcd0d/a/zxDDJYe
  - name: Contact 
    link: https://www.sketch.com/s/dd2f2e71-977c-45b4-baf3-8bf823bfcd0d/a/ZOD2GMG
  - name: Find Help
    link: https://www.sketch.com/s/dd2f2e71-977c-45b4-baf3-8bf823bfcd0d/a/ZOkkZqa
  - name: About
    link: https://www.sketch.com/s/dd2f2e71-977c-45b4-baf3-8bf823bfcd0d/a/JnV5z45
---
### Each list item
{% include partials/content-specs.md content=page.specs2 %} 

## Functionality Specifications
This section show the details on how to build the page based on the author selections.

### Page Header
The page header includes the Title, Summary and the Help CTA cards. 
- **The CTA Cards** are optional, the author my choose one or both. If they chose 1, the CTA shows to the right of the summary, each taking 50% of the space. If they choose both, the summary text displays first (at no more than 80ex), with both CTAs beneath. Examples of this can be seen on the [Find Help](https://www.sketch.com/s/dd2f2e71-977c-45b4-baf3-8bf823bfcd0d/a/ZOkkZqa) and [Contact](https://www.sketch.com/s/dd2f2e71-977c-45b4-baf3-8bf823bfcd0d/a/ZOD2GMG) concepts.
- **Header Background**: If the blueground option is turned on, the page header displays the background with the bottom border.

### Page Body
The page body contains the body, accordions and vertical tabs. All of these elements are optional, although the author can choose either the accordion or the vertical tabs, not both.
- the body displays first with a max-width of 80ex.
- the author can choose either the accordion or the vertical tabs, not both. The list content is used to fill the pattern using the label, title (h2), and content.



