---
layout: default
title: Washington
categories: [prototype]
type: [sub-nav-item, prototype]
permalink: /prototype/states/detail
summary: State Detail
search_type: all

body: |
  brief explainer text about what to expect here -- Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 

accordion:
  - title: Adoption and Guardianship Questions

accordions:
  - title: Inner Accordion title 1
    content: explainer text about what to expect here -- Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 
  - title: Inner Accordion title 2
    content: explainer text about what to expect here -- Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 
  - title: Inner Accordion title 3
    content: explainer text about what to expect here -- Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 
  - title: Inner Accordion title 4
    content: explainer text about what to expect here -- Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 
---
{% include patterns/breadcrumb/breadcrumb-jk.md %}
<div class="grid-container" markdown=1>
# {{ page.title }}
<div class="usa-intro">{{ page.body }}</div>

<div class="usa-accordion accordion" style="margin-bottom: 60px;">
    {% for item in page.accordion %}
        <h2 class="usa-accordion__heading">
            <button
            class="usa-accordion__button"
            aria-expanded="false"
            aria-controls="a{{forloop.index}}"
            >
                {{ item.title }}
            </button>
        </h2>
        <div id="a{{forloop.index}}" class="usa-accordion__content usa-prose">
            <h4>Section Title</h4>
            <div class="usa-accordion accordion">
                {% for items in page.accordions %}
                    <h4 class="usa-accordion__heading">
                        <button
                        class="usa-accordion__button"
                        aria-expanded="false"
                        aria-controls="b{{forloop.index}}"
                        >
                          {{ items.title }}
                        </button>
                    </h4>
                    <div id="b{{forloop.index}}" class="usa-accordion__content usa-prose">
                        {{ items.content }}
                    </div>
                {% endfor %}
            </div>
            <h4>Section Title</h4>
            <div class="usa-accordion">
                {% for items in page.accordions %}
                    <h4 class="usa-accordion__heading">
                        <button
                        class="usa-accordion__button"
                        aria-expanded="false"
                        aria-controls="c{{forloop.index}}"
                        >
                          {{ items.title }}
                        </button>
                    </h4>
                    <div id="c{{forloop.index}}" class="usa-accordion__content usa-prose">
                        {{ items.content }}
                    </div>
                {% endfor %}
            </div>
        </div>
    {% endfor %}
</div>
</div>

{% include prototype/search-results.md %}
