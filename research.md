---
layout: page
title: Research
permalink: /research/
---
<ul>{% for i in site.data.interests %}<li>{{ i }}</li>{% endfor %}</ul>

<h2>Publications</h2>
{% assign fin = site.publications | where: "field", "finance" %}
{% include collection-list.html docs=fin %}

<h2>Other publications</h2>
{% assign oth = site.publications | where: "field", "other" %}
{% include collection-list.html docs=oth %}

<h2>Working papers</h2>
{% assign wp = site.workingpapers | where_exp: "d", "d.wip != true" %}
{% include collection-list.html docs=wp by="order" %}

{% comment %}Hidden for now; remove the comment tags to show again.
<h2>Work in progress</h2>
{% assign wip = site.workingpapers | where: "wip", true %}
{% include collection-list.html docs=wip by="order" %}
{% endcomment %}

<h2>Earlier work in physics</h2>
{% assign phys = site.publications | where: "field", "physics" %}
{% include collection-list.html docs=phys %}
