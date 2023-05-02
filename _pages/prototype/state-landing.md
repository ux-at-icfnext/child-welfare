---
layout: default
title: Find Information by State
categories: [prototype]
type: [sub-nav-item, prototype]
permalink: /prototype/states/landing
summary: State landing
body: |
  brief explainer text about what to expect here -- Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 

map:
  - name: States
  - name: Territories
  - name: Tribes
states:
  - name: Alabama (AL)
  - name: Alaska (AK)
  - name: American Samoa (AS)
  - name: Arizona (AZ)
  - name: Arkansas (AR)
  - name: California (CA)
  - name: Colorado (CO)
  - name: Connecticut (CT)
  - name: Delaware (DE)
  - name: District of Columbia (DC)
  - name: Florida (FL)
  - name: Georgia (GA)
  - name: Guam (GU)
  - name: Hawaii (HI)
  - name: Idaho (ID)
  - name: Illinois (IL)
  - name: Indiana (IN)
  - name: Iowa (IA)
  - name: Kansas (KS)
  - name: Kentucky (KY)
  - name: Louisiana (LA)
  - name: Maine (ME)
  - name: Maryland (MD)
  - name: Massachusetts (MA)
  - name: Michigan (MI)
  - name: Minnesota (MN)
  - name: Mississippi (MS)
  - name: Missouri (MO)
  - name: Montana (MT)
  - name: Nebraska (NE)
  - name: Nevada (NV)
  - name: New Hampshire (NH)
  - name: New Jersey (NJ)
  - name: New Mexico (NM)
  - name: New York (NY)
  - name: North Carolina (NC)
  - name: North Dakota (ND)
  - name: Northern Mariana Islands (MP)
  - name: Ohio (OH)
  - name: Oklahoma (OK)
  - name: Oregon (OR)
  - name: Pennsylvania (PA)
  - name: Puerto Rico (PR)
  - name: Rhode Island (RI)
  - name: South Carolina (SC)
  - name: South Dakota (SD)
  - name: Tennessee (TN)
  - name: Texas (TX)
  - name: Utah (UT)
  - name: Vermont (VT)
  - name: Virgin Islands (VI)
  - name: Virginia (VA)
  - name: Washington (WA)
  - name: West Virginia (WV)
  - name: Wisconsin (WI)
  - name: Wyoming (WY)

---
{% include patterns/breadcrumb/breadcrumb-jk.md %}
<div class="grid-container" markdown=1>

# {{ page.title }}

{{ page.body }}

<div class="map">
  <p>choose your state, territory, or tribe below:</p>

  <div class="grid-row grid-gap">
    <div class="tablet:grid-col-4" style="align-items: center;" > 
      <span style="margin-bottom: 1.25rem">
      <select class="usa-select" name="map-choices" id="map-choices">
        <option value="volvo">States</option>
        {% for m in page.map %}
        <option value="saab">{{ m.name }}</option>
        {% endfor %}
    </select>
    </span>
    <span>
      <select class="usa-select" name="map-choices" id="map-choices">
        <option value="volvo">--Select--</option>
        {% for s in page.states %}
        <option value="saab">{{ s.name }}</option>
        {% endfor %}
      </select>
      </span>
    </div>
    <div class="tablet:grid-col-8"><img src="/assets/icons/prototype/map.png" /></div>

  </div>
</div>

</div>