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

{% endcomment %}

{% for work in site.data.citations %}
  {% include citation.html lookup=work.id style="rich" %}
{% endfor %}