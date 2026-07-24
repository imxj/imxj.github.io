---
layout: default
permalink: /
---

{% capture home_content %}
{% include_relative README.md %}
{% endcapture %}
{{ home_content | markdownify }}
