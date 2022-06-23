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

{% assign y = {{page.title}} | prepend: 'site.data.' %}
{{y}}
{{site.data[page.title]}}
{% capture x %}
{% include tablegen.html i = y %} 
{% endcapture %}



<table style = "margin-left:10px">
  <tr>
    <th> Parameter </th>
    <th> value </th>
  </tr>
  <tr>
     
     {% include tablegen.html i = {{site.data[page.title]}} %} 
  </tr>
</table>
