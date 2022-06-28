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
stuff:
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

{% capture y %}
site.data.{{page.title]}}
{% endcapture %}

{% include tbheadgen.html x = page.stuff %} 

