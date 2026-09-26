---
layout: page
title: CV
permalink: /cv/
---
<p><a href="{{ site.author.cv | relative_url }}">Download full CV (PDF)</a></p>

<h2>Appointments</h2>
{% for p in site.data.positions %}
<p><strong>{{ p.org }}</strong><br>
{% for r in p.roles %}{{ r.title }} <span class="muted">({{ r.when }})</span>{% unless forloop.last %}<br>{% endunless %}{% endfor %}</p>
{% endfor %}

<h2>Education</h2>
<ul>{% for e in site.data.education %}<li>{{ e.degree }}, {{ e.school }} <span class="muted">({{ e.year }})</span></li>{% endfor %}</ul>

<h2>Awards and grants</h2>
<ul>{% for a in site.data.awards %}<li>{{ a.title }} <span class="muted">({{ a.year }})</span></li>{% endfor %}</ul>

<h2>Professional service</h2>
<p><strong>Institutional</strong></p>
<ul>{% for s in site.data.service.institutional %}<li>{{ s }}</li>{% endfor %}</ul>
<p><strong>Conference organization</strong></p>
<ul>{% for s in site.data.service.conferences %}<li>{{ s }}</li>{% endfor %}</ul>
<p><strong>Ad hoc referee:</strong> {{ site.data.service.referee | join: "; " }}.</p>
