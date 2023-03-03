---
layout: template
categories: [templates, resource-detail]
type: [detail-page]
title: Podcast Resources
permalink: /templates/resource/podcast
overview: Details about the Podcast resource type
description: Details about the Podcast resource type

specs: 
  - name: Episode link
    type: Soundcloud link
    authored: yes
    required: yes
  - name: Length
    type: time
    notes: length should be pulled from the soundcloud info
  - name: Transcript
    type: file upload - PDF
    authored: yes
    required: yes
  - name: File size
    type: number  
    notes: file size should be from the PDF
  
---

## Page Header
- Date label used: "Date"
- Length: Uses length of podcast

## Podcast Resource
Uses SoundCloud embedded player.

**Transcript Link:** Shows Episode name, and PDF size
- onclick of link, PDF opens/or downloads according to browser preferences

