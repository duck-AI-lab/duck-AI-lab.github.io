---
---
About DUCK LAB

{% comment %}
{% include section.html %}
## Highlights
{% endcomment %}

{% comment %} --- 1. RESEARCH SECTION --- {% endcomment %}
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

{% comment %} --- 2. PROJECTS SECTION (Custom Stacked HTML) --- {% endcomment %}

<div class="feature-container" style="display: flex; flex-direction: row-reverse; gap: 3rem; align-items: center; margin: 4rem 0 6rem 0;">
  
  <div class="feature-image-stack" style="flex: 1; position: relative;">
    <a href="projects" style="display: block; position: relative;">
      
      <img src="images/projects/road_demo.gif" alt="ROAD-R Demo" style="width: 100%; display: block; border-radius: 12px; box-shadow: 0 4px 10px rgba(0,0,0,0.1);">
      
      <img src="images/projects/pishield_logo.png" alt="PiShield Logo" style="position: absolute; bottom: -25px; right: -25px; width: 40%; filter: drop-shadow(0 8px 20px rgba(0,0,0,0.4)); border-radius: 12px; border: 2px solid white;">
    </a>
  </div>

  <div class="feature-content" style="flex: 1; padding: 1rem;">
    <h2 style="margin-top: 0;">Projects</h2>
    <p>Developed projects.</p>
    
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
      /* Reset margin on mobile */
      margin-bottom: 4rem !important;
    }
    /* On mobile, center the stack and reduce offset so it doesn't go offscreen */
    .feature-image-stack img:nth-child(2) {
        bottom: -15px !important;
        right: -10px !important;
        width: 35% !important;
    }
  }
</style>

{% comment %} --- 3. TEAM SECTION --- {% endcomment %}
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