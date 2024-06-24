---
permalink: /projects/
title: "projects"
author_profile: true
layout: default
# redirect_from: 
#   - /projects/
#   - /projects.html
---
{{ site.repository }}
{{ gsDataBaseUrl }}
{{ url }}

{% if site.google_scholar_stats_use_cdn %}
  {% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
  {% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}
<span class='anchor' id='projects'></span>

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}