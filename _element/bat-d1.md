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
---

{% capture y %}
{{site.data.[page.title]| slugify }}
{% endcapture %}

{% capture x %}
{% include tablegen.html i =site.data.bat-d1%} 
{% endcapture %}

{{y}}

{% for test in k %}
{{test}}<br>
<br>


{% endfor %}

{% include tbheadgen.html x = y %} 

