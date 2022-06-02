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
      <tr>
      {% if var.first %}
        {% for svar in var %}
        <tr>
          <td>{{svar}} </td>
        </tr> 
        {% endfor %}
      {% else %}
          <td> {{var}} </td>
      {% endif %}
      </tr>
    {% endfor %}  
  {% endfor %}
</table>
