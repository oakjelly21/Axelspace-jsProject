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

{% assign y = site.data | append: {{page.title}} %}
{{y}}

{% capture x %}
{% include tablegen.html i = site.data.bat-d1 %} 
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
