---
layout: default
title: Home
---
<div class="profile">
  <img src="{{ site.author.photo | relative_url }}" alt="{{ site.author.name }}">
  <div>
    <h1>{{ site.author.name }}</h1>
    <p>{{ site.author.title }}, {{ site.author.department }}<br>
    <a href="{{ site.author.university_url }}">{{ site.author.school }}</a>, {{ site.author.university }}</p>
    <address>
      {{ site.author.office }}<br>{{ site.author.address }}<br>{{ site.author.phone }} ·
      <a href="mailto:{{ site.author.email }}">{{ site.author.email }}</a>
    </address>
    <p><a href="{{ site.author.profile_url }}">UCalgary profile</a> ·
       <a href="{{ site.author.scholar_url }}">Google Scholar</a> ·
       <a href="https://github.com/{{ site.author.github }}">GitHub</a></p>
  </div>
</div>

<aside class="focus">
  <h2>My Research</h2>
  <p>I study how innovative technologies such as quantum computing, blockchain and distributed ledgers change financial
  infrastructure, and what that means for banks, markets and regulation. I come to these questions from
  practice: before joining Calgary I was Senior Architect for the Digital Euro (CBDC) at the
  Deutsche Bundesbank, where I worked on the design, security and resilience of a central bank
  digital currency. My research asks about the economic repercussions of such design choices.</p>
</aside>

<h2>Research interests</h2>
<ul>{% for i in site.data.interests %}<li>{{ i }}</li>{% endfor %}</ul>

<h2>Selected publications</h2>
{% assign pubs = site.publications | where: "field", "finance" | sort: "year" | reverse %}
{% for doc in pubs %}{% include entry.html item=doc %}{% endfor %}
<p><a href="{{ '/research/' | relative_url }}">All research →</a></p>
