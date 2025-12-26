---
---
About DUCK LAB


{% comment %}
{% include section.html %}
## Highlights
{% endcomment %}

{% capture text %}

[//]: # (Recent publications.)

{%
  include button.html
  link="research"
  text="See our publications"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/photo.jpg"
  link="research"
  title="Research"
  text=text
%}

{% capture text %}

[//]: # (Developed projects.)

<div class="feature-container" style="display: flex; flex-direction: row-reverse; gap: 2rem; align-items: center; margin: 4rem 0;">
  
  <div class="feature-image" style="flex: 1; position: relative; border-radius: 12px; overflow: hidden; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
    <a href="projects" style="display: block; position: relative;">
      <img src="images/projects/road_demo.gif" alt="ROAD-R Demo" style="width: 100%; display: block; opacity: 0.9;">
      <img src="images/projects/pishield_logo.png" alt="PiShield Logo" style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 45%; filter: drop-shadow(0 5px 15px rgba(0,0,0,0.5));">
    </a>
  </div>

  <div class="feature-content" style="flex: 1; padding: 1rem;">
    <h2 style="margin-top: 0;">Projects</h2>
    
    {%
      include button.html
      link="projects"
      text="Browse our projects"
      icon="fa-solid fa-arrow-right"
      flip=true
      style="bare"
    %}
  </div>

</div>

<style>
  @media (max-width: 768px) {
    .feature-container {
      flex-direction: column !important;
      text-align: center;
    }
  }
</style>

{%
  include feature.html
  image="<div style='position: relative; width: 100%; border-radius: 12px; overflow: hidden; box-shadow: 0 4px 6px rgba(0,0,0,0.1);'><img src='images/projects/road_demo.gif' style='width: 100%; display: block; opacity: 0.9;' alt='ROAD-R Demo'><img src='images/projects/pishield_logo.png' style='position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 45%; filter: drop-shadow(0 5px 15px rgba(0,0,0,0.5));' alt='PiShield Logo'></div>"
  link="projects"
  title="Projects"
  flip=true
  style="bare"
  text=text
%}

{% capture text %}

[//]: # (Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.)

{%
  include button.html
  link="team"
  text="Meet the team"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/photo.jpg"
  link="team"
  title="Team"
  text=text
%}
