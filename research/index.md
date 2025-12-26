---
title: Research
nav:
  order: 1
  tooltip: Published works
---

# {% include icon.html icon="fa-solid fa-lightbulb" %}Research   

{% comment %}
# {% include icon.html icon="fa-solid fa-microscope" %}Research
{% include section.html %}
## All
{% include search-box.html %}
{% include search-info.html %}

{% include list.html data="citations" component="citation" style="rich" %}
## All

{% for work in site.data.citations %}
  {% include citation.html lookup=work.id style="rich" %}
{% endfor %}
{% endcomment %}


 
{% assign citations = site.data.citations %}

{% comment %} 1. Group citations by Year (2025, 2024...) {% endcomment %}
{% assign grouped_citations = citations 
  | group_by_exp: "item", "item.date | date: '%Y'" 
  | sort: "name" 
  | reverse 
%}

{% comment %} 2. Loop through each Year {% endcomment %}
{% for year in grouped_citations %}
  
  <h2 id="{{ year.name }}" style="margin-top: 40px; margin-bottom: 20px;">{{ year.name }}</h2>

  
  {% for work in year.items %}
    {% include citation.html lookup=work.id style="rich" %}
  {% endfor %}

{% endfor %}