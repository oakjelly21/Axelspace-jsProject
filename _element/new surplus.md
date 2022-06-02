---
title: "new surplus"
layout: single
experimental: false
tech-std: false
non tech-std: false
mech: true
elec: false
---

hello world  

<table style = "margin-left:10px">
  <tr>
    <th> a </th>
    <th> b </th>
  </tr>
  {% for bat in site.data.bats %}
    {% for var in bat %}
      {% if var.first %}
        <tr> 
          <td>{{var}} </td>
        </tr>
      {% else %}
        <tr>
          
        </tr>
      {% endif %}
    {% endfor %}  
  {% endfor %}
</table>
