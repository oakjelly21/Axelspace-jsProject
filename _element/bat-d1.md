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

{% capture x %}
{% include tablegen.html i = site.data.bat-d1 %} 
{% endcapture %}


{{x}}

<table style = "margin-left:10px">
  <tr>
    <th> Parameter </th>
    <th> value </th>
  </tr>
  <tr>
     
     {% include tablegen.html i = site.data.bat-d1 %} 
  </tr>
</table>
