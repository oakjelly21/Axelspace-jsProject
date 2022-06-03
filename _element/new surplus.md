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
  <tr>
    {% for var in bat %} 
      {% if var.first %}
        <tr>
        {% for svar in var %}
            {% if svar.first %}
             <tr>
                  {% for ssvar in svar %}
                      <tr>
                        <td>{{ssvar}}</td>
                      </tr>
                   {% endfor %}
               {% else %}
                <td>{{svar}}</td>
              {% endif %}
            </tr>
        {% endfor %}  
        </tr> 
       {% endfor %}
      {% else %}
          <td> {{var}} </td>
      {% endif %}
   {% endfor %}   
  </tr>
  {% endfor %}
</table>
