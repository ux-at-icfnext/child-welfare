---
layout: template
categories: [templates, resource-detail]
type: [detail-page]
title: Video Resources
permalink: /templates/resource/video
overview: Details about the video resource type
description: Details about the video resource type

specs: 
  - name: Episode link
    type: Youtube link
    authored: yes
    required: yes
  - name: Length
    type: time
    notes: length should be pulled from the youtube info
  - name: ADA Episode link
    type: Youtube link
    authored: yes
    required: yes
  - name: Transcript
    type: file upload - PDF
    authored: yes
    required: yes
  - name: File size
    type: number  
    notes: file size should be from the PDF
  - name: Audio Description
    type: file upload - PDF
    authored: yes
    required: yes
  - name: Audio File size
    type: number  
    notes: file size should be from the PDF
---

## Page Header
- Date label used: "Date"
- Length: Uses length of video

## Video Resource
- Uses YouTube embedded player.
- Show the Regular and ADA video side by side at 45% width each

Transcript Link: Shows Episode name, and PDF size
- onclick of link, PDF opens/or downloads according to browser preferences

Audio Description: Show Espisode name, "audio description"
- onclick of link, PDF opens/or downloads according to browser preferences

