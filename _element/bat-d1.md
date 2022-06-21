---
title: "bat-d1"
layout: 'single'
aocs: 'false'
eps: 'true'
cdh: 'false'
comm: 'false'
str: 'false'
mission: 'false'
---

{% assign y = {{page.title}} %}
{{y}}

{% capture x %}
{% include tablegen.html i = y %} 
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
