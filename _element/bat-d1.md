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
{% include tablegen.html i = site.data.{{page.title}}.yml %} 
{% endcapture %}



<table style = "margin-left:10px">
  <tr>
    <th> Parameter </th>
    <th> value </th>
  </tr>
  <tr>
     
     {{x}}
  </tr>
</table>
