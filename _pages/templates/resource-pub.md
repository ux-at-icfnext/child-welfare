---
layout: template
categories: [templates, resource-detail]
type: [detail-page]
title: Publication Resources
permalink: /templates/resource/pub
overview: Details about the publication resource type
description: Details about the publication resource type

specs:
  - name: File
    type: file upload
    authored: yes
    required: yes
    content: Limit 1
  - name: File size
    type: number  
    notes: file size should be from the PDF
  - name: Additional files
    type: file upload
    authored: yes
  - name: Series Title
    type: text
    authored: yes
  - name: Author
    type: text
    authored: yes
    required: yes
  - name: Year Published
    type: text
    authored: yes
    required: yes
  - name: Current through
    type: date
  - name: Order online
    type: toggle
    content: default to false
  - name: Download by Language
    type: multi-select
    content: "Options: English, Spanish"
  - name: Download Image sizes
    type: array
    notes: author can add the image size variations -- for example 250x300, 500x600
  

---

## Page Header
- Date field is hidden
- Length field is hidden

## Publication Resource
- Thumbnail of resource image
- Series title
- Year Published
- Current Through:

Action buttons:
Available both English and Spanish: 
- Shows the combo download button. With the text "Download (PDF {size})"
- aria-label included file name: "Download {file name} (PDF {size})"
- OnClick of button, language options are displayed
- OnClick of language option, PDF opens/or downloads according to browser preferences

Available in either English or Spanish
- Shows the single download button
- aria-label included file name: "Download {file name} (PDF {size})"
- OnClick of language option, PDF opens/or downloads according to browser preferences

If available to order online
- Shows the Order online button: "Order online for free"
- aria-label: " "Order {file name } online for free"
- OnClick