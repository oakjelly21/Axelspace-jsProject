---
title: "rework_protocol"
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
  {% for bat in site.data.bats2 %}
  <tr>
    <td> {{bat.a}} </td>
    <td> {{bat.b}} </td>
  </tr>
  {% endfor %}
</table>
