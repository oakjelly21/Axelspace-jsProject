---
title: "new surplus"
layout: single
experimental: false
tech-std: false
non tech-std: false
mech: true
elec: false
---

lorem ipsum
<table>
  <tr>
    <th> a </th>
    <th> b </th>
    <th> c </th>
    <th> d </th>
  </tr>
  {% for bat in site.data.bats %}
  <tr>
    <td> {{bats.a}} </td>
    <td> {{bats.b}} </td>
    <td> {{bats.c}} </td>
    <td> {{bats.d}} </td>
  </tr>
  {% endfor %}
</table>
