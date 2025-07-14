---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% assign working_papers = site.research | where: "type", "working" %}
{% assign publications = site.research | where: "type", "publication" %}
{% assign work_in_progress = site.research | where: "type", "progress" %}

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