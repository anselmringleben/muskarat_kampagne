---
layout: default
---
## Test

<div align="center">
  <img src="assets/img/shapes.png" width="487" height="271" alt="Shapes" usemap="#shapesmap"> 
  <map name="shapesmap">
    <area shape="rect" coords="29,32,230,215" href="square.html" alt="Square">
    <area shape="circle" coords="360,130,100" href="circle.html" alt="Circle">
  </map>
</div>

# Include

* {% include person_url.html name="Mutadin" %}
  {% include person.html name="Farid Abu Musa" list_item=true %}

{% include person.html name="Farid Abu Musa" %}

# Collection access

{% for person in site.people %}
  <h2>Person</h2>
  <h3>{{ person.name }} - {{ person.position }}</h3>
  <p>{{ person.content | markdownify }}</p>
{% endfor %}