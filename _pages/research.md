---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

My research interests are banking, corporate finance, and digital payments.

### Working papers

{% for post in site.workingpapers reversed %}
  {% include archive-single.html %}
{% endfor %}

### Work in progress


### Publications

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}





