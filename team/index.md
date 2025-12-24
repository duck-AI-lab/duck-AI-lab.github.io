---
title: Team
nav:
  order: 3
  tooltip: About our team
---

# Team
{% comment %}
# {% include icon.html icon="fa-solid fa-users" %}Team

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
{% endcomment %}


{% include section.html %}

{% comment %}
{% include list.html data="members" component="portrait" filter="role == 'pi'" %}
{% include list.html data="members" component="portrait" filter="role != 'pi'" %}

{% comment %}
## Principal Investigator
{% include list.html data="members" component="portrait" filter="role == 'professor'" %}

## Postdoctoral Researchers
{% include list.html data="members" component="portrait" filter="role == 'postdoc'" %}

## PhD Students
{% include list.html data="members" component="portrait" filter="role == 'phd'" %}
{% endcomment %}


## Principal Investigator
{% include list.html data="members" component="member-bio" filter="role == 'pi'" %}

## Postdoctoral Researchers
{% include list.html data="members" component="member-bio" filter="role == 'postdoc'" %}

## PhD Students
{% include list.html data="members" component="member-bio" filter="role == 'phd'" %}


{% comment %}
{% include section.html background="images/background.jpg" dark=true %}

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.



{% include section.html %}
{% endcomment %}

{% capture content %}

{% comment %}

{% include figure.html image="images/photo.jpg" %}
{% include figure.html image="images/photo.jpg" %}
{% include figure.html image="images/photo.jpg" %}
{% endcomment %}

{% endcapture %}

{% include grid.html style="square" content=content %}
