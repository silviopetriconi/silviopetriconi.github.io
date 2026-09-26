---
layout: page
title: Talks
permalink: /talks/
---
Conference and seminar presentations (including discussions).

{% assign years = site.talks | sort: "year" | reverse %}
<dl class="talks">
{% for y in years %}
  <dt>{{ y.year }}</dt>
  <dd>{{ y.venues | join: "; " }}</dd>
{% endfor %}
</dl>
