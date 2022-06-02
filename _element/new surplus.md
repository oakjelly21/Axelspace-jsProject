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
  <tr> {{bat.size}}</tr>
  <tr>
    {% for col in bat%}
    <tr> {{col.size}}</tr>
    <td> {{col}} </td>
      {% for scol in col%}
      <td> {{scol}} </td>
      {% endfor %}
    {% endfor %}
  </tr>
  {% endfor %}
</table>
