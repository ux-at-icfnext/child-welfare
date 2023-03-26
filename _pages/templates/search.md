---
layout: template
categories: [templates, searchresults]
type: [sub-nav-item, variations]
title: Search
permalink: /templates/searchresults
overview: Search pages are mostly dynamic.
description: Search pages are mostly dynamic, there are several search pages through out the site. These include, the Global Search, All Resources, Event Search, Directory, and Subtopics. They all share the same basic functionality.

spec:
  - name: Page Title
    type: h1
    required: yes
    authored: yes
  - name: Summary
    type: meta description
    content: 250 characters max
    required: yes
    authored: yes
  - name: Body
    type: rich text
    content: 200 word max recommended
  - name: Pullquote
    type: pull-quote
    content: 250 characters max
  - name: Quicklinks
    type: href
    content: link url, link text
    note: module is optional -- limit 5 links
    
spec2:
  - name: Format Type
    authored: dynamic
    required: if not available, format type does not display on the item
    type: text + icon
    source: resouce detail-format
  - name: Title
    type: h3
    authored: dynamic
    source: resouce detail-title
  - name: Source
    type: text
    authored: dynamic
    required: if not available, format type does not display on the item
    source: resouce detail-source
  - name: Source
    type: text
    authored: dynamic
    content: 250 characters max
    source: resouce detail-summary
  - name: link
    type: href
    authored: dynamic
    source: resouce detail-url

components:
  - title: Collection pattern
    link: /patterns/collection/
  - title: Accordion
    link: /patterns/accordion
  - title: Pagination
    link: /patterns/pagination
  - title: Search widget
    link: /patterns/search/
      
---

## Search Page functionality – onLoad
On page load, content is sorted by Latest Published and 15 items are displayed.
There are three types of incoming searches, canned, keyword, empty.

#### Empty -
a user submits an empty search (search from with blank input field)
In this instance, the search page is displayed without out any filters applied.

#### Keyword -
Any search using the search module, results are constrained to keyword matches.

#### Canned -
Authors should be able to create links in the site to a prefiltered search result. For this functionality to work, search terms and filters need to be added to the url.

## Page Header
_note_ [Subtopics Pages](/templates/subtopic-page) has it's own page header. Please see the specifications for how that page functions.

{% include partials/content-specs.md content=page.spec %}

**Quick Links**
If author adds quick links to the page, the module sits to the right of the page body on larger screens, and below the body on mobile

## Filters
Filters are chosen according to taxonomy. Please see content strategy to connect filters with filter types.
### Overall Functionality
- OnLoad all accordions are in the closed position
- OnTap/Click of of accordion item, that item opens to display inner content.
- OnTap/Click again, the item closes to hide content.

SM & MD Breakpoints:
- OnLoad, the whole filter module is hidden except for the title & filter icon.
- OnTap of title or icon the module slides open and pushes the content down.
- OnTap again, the module slides close and content is brought back up.
LG+ Breakpoints:
- OnLoad the filter module is displayed

|![Search Controls on small screens](/assets/icons/spec-images/search-controls-mobile.png)|
|:--:|
| <b>small screen filters with view controls</b>|

### Filter types
1) Date Range Filter
On Default,
- "From" date is set to the earliest date of all items
- "To" date is set to current year.
On select of either year, result set is filtered to new date range.

![Date Range Filter](/assets/icons/spec-images/publication.png)

2) Single-select Filter
- Selection list is presented as a radio option list
- OnTap/Click of a radio button other selected radio buttons become unselected, filter is applied to result set
- OnTap/Click of a selected radio button, deselects button and result set is updated

![Single Select](/assets/icons/spec-images/resources.png)

3) Multi-select Filter
- Selection list is presented as a check option list
- OnTap/Click of a checkbox, filter is applied to result set
- Number of results matching the checkbox options are updated
- Options that are no longer in the result set are grayed out and disabled

![Multi-select](/assets/icons/spec-images/source.png)

4) Location Filter
_This assumes multiple location types, such as states, terrorites, tribes, regions_
- OnTap/Click of child term, accordion opens to display children.
- A max of 15 items should display, then list is scrollable to view more.
- OnClick of grandchild term, filter is applied to result set.
- On Next Tap/Click of child term, accordion closes to hide children.

![Location Filter](/assets/icons/spec-images/location.png)

### Clear
OnTap/Onclick of "Clear Filters" all filters are removed and result set is restrained only by keywords.

## View Controls
1) Search box
- If keyword present, shows current keyword, other wise shows "Search by keyword"
- On click of search icon button, search filters on key words added to search box (note - if no term was entered, page just returns all results [there is no error state])

2) Sort by:
Options:
- Relevance (Default)
- Latest Published 
- A - Z
On select of sort by, result set is reordered by chosen method.

2) View
View line shows the total number of results.
View Options:
- 15 (default)
- 50
- 100
- On select of view number, system displays the number of items chosen.

![Search Controls](/assets/icons/spec-images/searchcontrols.png)

## Pagination
uses [pagination pattern](/patterns/pagination/)

## Result item
_See variations for other layout options_
### Default layout
uses the [Collections pattern](/patterns/collection/)
{% include partials/content-specs.md content=page.spec2 %}

![example](/assets/icons/spec-images/result-example.png)