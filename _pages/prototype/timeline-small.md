---
layout: default
title: Children’s Bureau Timeline
categories: [prototype]
type: [sub-nav-item, prototype]
permalink: /prototype/timeline-small
summary: |
  Use this interactive timeline to explore the Children’s Bureau’s rich history, decade by decade. Learn about the key political and social events that influenced the development of today’s Children’s Bureau and shaped the evolution of child welfare in America.
---
<style>
    #value2:checked ~ .text-content .tab1,
    #value3:checked ~ .text-content .tab1 {
    display: none;
    }
    #value1:checked ~ .tab1{
        display: block;
    }
</style>

{% include patterns/breadcrumb/breadcrumb-jk.md %}
<div class="grid-container" style="margin-top: 40px;">
  <h1>{{ page.title }}</h1>
  <div class="usa-intro">{{ page.summary }}</div>
</div>
<div class="grid-container">
    <form class="usa-form select">
    <select class="usa-select" name="options" id="options" style="border: none; border-top: 1px solid lightgray; border-bottom: 1px solid lightgray; font-weight: bold;">
        <option value="value1" id="value1">1854 - 1912</option>
        <option value="value2" id="value2">1913 - 1922</option>
        <option value="value3" id="value3">1923 - 1932</option>
    </select>
    </form>
    <div class="text-content">
        <div class="tab1 text">
            {% include prototype/timeline/accordion.md %}
        </div>
    </div>
</div>