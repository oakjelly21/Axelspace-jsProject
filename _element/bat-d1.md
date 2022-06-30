---
title: "bat-d1"
ymlfile: site.data.bat-d1.yml
layout: 'single'
aocs: 'false'
eps: 'true'
cdh: 'false'
comm: 'false'
str: 'false'
mission: 'false'
data:
    -頭字語 /Acronym: BAT
    -機器概説 /Device Outline: Battery
    -帰属 /Subsystem: EPS
    -内部冗長の有無 /Redundancy in the Device: 無し
    -Basic information:
        -主要諸元/Main specifications:
            -外観/Appearance: Left one BAT appearance.<br>The image of BAT after being installed on inner structure. Just for reference.<br><img src = "/assets/bat1.jpg"><img src = "/assets/bat2.jpg">
            -構成・内部配置/Configuration(internal structure): 筐体内に基板を搭載
            -機能/Functions: 1)太陽電池から供給される電力を蓄積する。<br>2)機器へ電力を供給する。
---


{% raw %}
<script>
    var diagramSource = 'title
__Hosted Payload Interface Diagram__
end title

scale 0.8
skinparam nodesep 30
skinparam ranksep 50
left to right direction

rectangle {
component Satellite {
  component Connector_S2PH
  component OBC
  component STR_PZ_Panel
  component Thermometer
  component Thermal_Insulator
  component Fasteners
  component Others
}
component GroundSystem
}
component Payload 
component PayloadUser
component Payload_Harness
together {
interface Electrical_Interface as "Electical\nI/F"
interface Data_Interface as "Data I/F"
interface Mechanical_Interface as "Thermal I/F\nStructural I/F"
interface Orbit_Interface as "Orbit I/F"
interface Electrical_Connector_Interface as  "Electrical\nConnector\nI/F"
interface Environmental_Interface as "Environmental\nI/F"
}
interface UserInterface as "User I/F"

PayloadUser -- UserInterface
UserInterface -- GroundSystem
GroundSystem -left- Satellite
OBC -- Connector_S2PH
OBC -- Electrical_Interface
OBC -- Data_Interface
Connector_S2PH -- Electrical_Connector_Interface
STR_PZ_Panel -- Mechanical_Interface
Thermometer -- Mechanical_Interface
Thermal_Insulator -- Mechanical_Interface
Fasteners -- Mechanical_Interface
Satellite -- Orbit_Interface
Satellite -- Environmental_Interface

Electrical_Connector_Interface -- Payload_Harness 
Payload_Harness -- Payload

Electrical_Interface -- Payload
Data_Interface -- Payload
Mechanical_Interface -- Payload
Orbit_Interface --Payload
Environmental_Interface --Payload'

    var data = textEncode(diagramSource) 
    var compressed = pako.deflate(data, { level: 9, to: 'string' }) 
    var result = btoa(compressed) 
      .replace(/\+/g, '-').replace(/\//g, '_') 
    var img = document.createElement("img");
    img.src = "https://kroki.io/plantuml/svg/" + result;
    document.body.appendChild(img);
</script>
{% endraw %}

