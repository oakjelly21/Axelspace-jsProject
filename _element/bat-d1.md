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

{{site.data[page.title]}}

{% capture x %}
{% include tablegen.html i ={{page.title}} %} 
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
