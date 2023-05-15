---
layout: default
title: Children’s Bureau Timeline
categories: [prototype]
type: [sub-nav-item, prototype]
permalink: /prototype/Timeline
summary: |
  Use this interactive timeline to explore the Children’s Bureau’s rich history, decade by decade. Learn about the key political and social events that influenced the development of today’s Children’s Bureau and shaped the evolution of child welfare in America.

---
<style>
.tabs {
  display: flex;
  align-items: top;
  justify-content: space-between;
}
.tabs .list{
    display: flex;
    flex-direction: column;
    position: relative;
    width: 20%;
    margin-right: 1rem;
  }
.tabs .list label {
  padding-block: .5rem;
  cursor: pointer;
  z-index: 12;
  /*add styling for tab here -->*/
}

.tabs .list label:hover {
  color: pink;
}

#tab1:checked ~ .list .tab1,
#tab2:checked ~ .list .tab2,
#tab3:checked ~ .list .tab3 {
  color: blue;
}

.tabs .indicator {
  position: absolute;
  height: 2rem; /* verify after styling list label */
  width: 100%;
  left: 0;
  top: 0;
  background-color: pink;
  transition: all 0.4s ease;
}
#tab1:checked ~ .list .indicator {
  top:0;
}
#tab2:checked ~ .list .indicator {
  top:2rem;
}
#tab3:checked ~ .list .indicator {
  top:4rem;
}
.tabs input[type="radio"] {
  display: none;
}
.tabs .text-content {
  width: 80%;
  height: 100%;
}
.tabs .text-content .text {
  display: none;
}

.tabs .text-content .tab1 {
  display: block;
}

#tab1:checked ~ .text-content .tab1,
#tab2:checked ~ .text-content .tab2,
#tab3:checked ~ .text-content .tab3 {
  display: block;
}

#tab2:checked ~ .text-content .tab1,
#tab3:checked ~ .text-content .tab1 {
  display: none;
}

</style>





<div class="grid-container">
  <h1>{{ page.title }}</h1>
  <div class="usa-intro">{{ page.summary }}</div>
</div>
<div class="grid-container">
<div class="tabs">
  <input type="radio" name="indicator" id="tab1">
  <input type="radio" name="indicator" id="tab2">
  <input type="radio" name="indicator" id="tab3">
  <div class="list">
    <label for="tab1" class="tab1" checked>1854 - 1912</label>
    <label for="tab2" class="tab2">1913 - 1922</label>
    <label for="tab3" class="tab3">1923 - 1932</label>
    <div class="indicator"></div>
  </div>
  <div class="text-content">
    <div class="tab1 text">
      {% include prototype/timeline/accordion.md %}
    </div>
    <div class="tab2 text">
      <div class="title">My Title Here (tab 2)</div>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Non doloribus eveniet possimus in distinctio ullam hic tempore sunt explicabo eum inventore consequuntur provident quia, fugit maxime facilis rem porro quis.</p>
    </div>
    <div class="tab3 text">
      <div class="title">My Title Here (tab 3)</div>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Non doloribus eveniet possimus in distinctio ullam hic tempore sunt explicabo eum inventore consequuntur provident quia, fugit maxime facilis rem porro quis.</p>
    </div>
  </div>
</div>
</div>
