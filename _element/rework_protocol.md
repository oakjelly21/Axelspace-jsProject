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

<table>
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
  <tr>
    <td> ![bat image 1](/assets/bat1.jpg) </td>
    <td> hello world </td>
  </tr>
</table>
