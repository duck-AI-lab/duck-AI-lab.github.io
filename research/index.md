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
{% assign years_to_display = "2026,2025,2024,2023,2022" | split: "," %}

{% for year in years_to_display %}
  
  {% comment %} Check if there are any papers for this year {% endcomment %}
  {% assign current_year_papers = citations | where_exp: "item", "item.date contains year" %}
  
  {% if current_year_papers.size > 0 %}
<h2 id="{{ year }}" style="margin-top: 40px; margin-bottom: 20px;">{{ year }}</h2>
    
    {% comment %} 
      Loop through the ORIGINAL citations.yaml to find matches.
      This ensures we strictly preserve the order from the file.
    {% endcomment %}
    {% for work in citations %}
      {% assign work_year = work.date | slice: 0, 4 %}
      {% if work_year == year %}
        {% include citation.html lookup=work.id style="rich" %}
      {% endif %}
    {% endfor %}
  {% endif %}

{% endfor %}