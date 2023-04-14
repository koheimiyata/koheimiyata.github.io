---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* B.S. in GitHub, Kansai University, 2010
* M.S. in Jekyll, Kagoshima University, 2012
* Ph.D in Version Control Theory, The University of Tokyo, 2015

Work experience
======
* Summer 2015: Research Assistant
  * Github University
  * Duties included: Tagging issues
  * Supervisor: Professor Git

  
Skills
======
* MATLAB
* Neuro imaging analysis
  * fMRI
  * DTI
  * EEG
* Motion capture analysis
  * DeepLabCut
  * OpenFace
  * OpenPose

Publications
======
  <ul>{% for post in site.publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Service and leadership
======
* Review Editor, Frontiers in Human Neuroscience | Interacting Minds and Brains 
* Manager, Japan Society for Dance Sciences
