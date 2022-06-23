---
title: "bat-d1"
ymlfile: site.data.bat-d1
layout: 'single'
aocs: 'false'
eps: 'true'
cdh: 'false'
comm: 'false'
str: 'false'
mission: 'false'
---

{% capture y %}
{{site.data.[page.title]}}
{% endcapture %}

{% capture x %}
{% include tablegen.html i =site.data.bat-d1%} 
{% endcapture %}

{% assign k = y |  split: ',' %}
{{y}}

{% for test in k %}
{{test}}<br>
<br>


{% endfor %}



<table style = "margin-left:10px">
  <tr>
    <th> Parameter </th>
    <th> value </th>
  </tr>
  <tr>
    {% include tablegen.html i = k %} 
     
  </tr>
</table>
