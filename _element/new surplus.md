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
  <td> {{bat.size}}</td>
  <td> {{bat[0].size}}</td>
  <td> {{bat[1].size}}</td>
  <tr>
    
    
    <td> {{bat[0]}} </td>
      
  </tr>
  {% endfor %}
</table>
