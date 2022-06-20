---
title: "bat-d1"
layout: single
experimental: false
tech-std: false
non tech-std: false
mech: true
elec: false
mission: false
---

{% assign x = {{page.title}} %}


{{x}}

<table style = "margin-left:10px">
  <tr>
    <th> Parameter </th>
    <th> value </th>
  </tr>
  <tr>
     
     {% include tablegen.html i = x %} 
  </tr>
</table>
