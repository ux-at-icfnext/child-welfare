---
layout: default
title: Hi! I'm a Glossary Page
categories: [prototype]
type: [sub-nav-item, prototype]
permalink: /prototype/glossary/
overview: This is example of a glosary example page.
summary: This is example of a glosary example page.
search: "search"
---
<div class="grid-container" markdown=1>

# Glossary

Many child welfare terms are subject to interpretation. The Glossary identifies commonly held definitions for terms that can be found on the Child Welfare Information Gateway website or in products and materials developed by external entities (e.g., Federal or State Agencies or other reliable organizations). When noted, Information Gateway is cited as the source. The Glossary also provides common acronyms and includes links to information on major Federal legislation and related child welfare terms. The Glossary will be updated as new terminology emerges in the field, as new legislation is enacted, and as child welfare terms take on new meaning.
{: .glossary-info}

<div markdown="1" class="glossary-search">
<div> 
{% include patterns/search/search-jk.md %}
</div>
<div><span class="current">A</span> B C D E F G H I J K L M N O P Q R S T U V W X Y Z</div>
</div>

{% for i in (1..20) %}
<div markdown="1" class="glossary-record">
## Term Name <i class="fa-solid fa-pipe"></i> Term Name (Spanish)
Term description — vitae nunc sed velit dignissim sodales ut eu sem integer vitae justo eget magna fermentum iaculis eu non diam phasellus vestibulum lorem sed risus ultricies tristique nulla aliquet enim tortor at auctor urna nunc id cursus metus aliquam eleifend mi in nulla posuere sollicitudin aliquam ultrices sagittis orci a scelerisque purus semper eget duis at tellus at urna condimentum mattis pellentesque id nibh tortor id aliquet lectus proin

[Link for more information at {source}](/) <i class="fa-solid fa-arrow-up-right-from-square"></i>
</div>
{% endfor %}
<div class="glossary-paging">
{% include patterns/pagination/pagination.md %}
</div>

</div>