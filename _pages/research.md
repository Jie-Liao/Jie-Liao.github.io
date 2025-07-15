---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

<!-- Debug: Check if research collection exists -->
<p>Total research items: {{ site.research.size }}</p>
{% for item in site.research %}
  <p>Found: {{ item.title }} (type: {{ item.type }})</p>
{% endfor %}

{% assign working_papers = site.research | where: "type", "working" %}
{% assign publications = site.research | where: "type", "publication" %}
{% assign work_in_progress = site.research | where: "type", "progress" %}

<p>Working papers: {{ working_papers.size }}</p>
<p>Publications: {{ publications.size }}</p>
<p>Work in progress: {{ work_in_progress.size }}</p>

{% if working_papers.size > 0 %}
## Working Papers

{% for post in working_papers %}
  {% include archive-single.html %}
{% endfor %}
{% endif %}

{% if publications.size > 0 %}
## Publications

{% for post in publications %}
  {% include archive-single.html %}
{% endfor %}
{% endif %}

{% if work_in_progress.size > 0 %}
## Work in Progress

{% for post in work_in_progress %}
  {% include archive-single.html %}
{% endfor %}
{% endif %} 