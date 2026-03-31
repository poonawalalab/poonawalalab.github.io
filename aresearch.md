---
layout: research
title: Research
permalink: /research/
---

## Research Overview

<p align="justify">
The Poonawala Lab works on assured learned controllers, with a particular focus on end-to-end systems where raw sensor data drives control decisions directly. 
We develop the stability conditions, data principles, and certification methods — rooted in dynamics and control theory — that make reliability in these systems something that can be reasoned about rather than merely observed.
</p>

We currently focus on the following applications:
1. Learning controllers for contact-rich manipulation
1. End-to-end controllers for navigation
1. Learning-enabled control for defect-free Additive Manufacturing 
1. Verification of learned neural network controllers

## Research Projects

<h3>Ongoing Projects </h3>
<!--div class = "justified"><p>Our current focus is on control and estimation algorithms for feedback loops that contain classifiers. We develop control-oriented machine learning algorithms that produce controllers/estimators with closed-loop performance guarantees. For autonomy, these controllers must be obtained on-line by systems that need them, necessitating automated methods for analysis and synthesis of such controllers.</p></div-->


<div class = "flex-container">
{% assign rtops = site.rtopics | sort: 'date' | reverse %}
{% for item in rtops %}
{% if item.status == "current" %}
  <div class = "thumby"><a href="{{ item.url | prepend:site.baseurl | prepend:site.url}}"><img src = "{{site.url}}/{{site.baseurl}}/assets/img/{{ item.thumb}}" width = "170px" height = "170px">
  <p>{% if item.short_title %}{{ item.short_title }}{% else %}{{ item.title }}{% endif %}</p>
  </a>
  </div>
{% endif %}
{% endfor %}
</div>



<h3>Completed Projects</h3>
<div class = "flex-container">
{% for item in site.rtopics %}
{% if item.status == "past" %}
  <div class = "thumby"><a href="{{ item.url | prepend:site.baseurl | prepend:site.url}}"><img src = "{{site.url}}/{{site.baseurl}}/assets/img/{{ item.thumb}}" width = "200px" height = "200px"><p>{% if item.short_title %}{{ item.short_title }}{% else %}{{ item.title }}{% endif %}</p></a> </div>
  {% endif %}
{% endfor %}
</div>

<h3>Projects Prior To UK</h3>
<div class = "flex-container">
{% for item in site.rtopics %}
{% if item.status == "preuk" %}
  <div class = "thumby"><a href="{{ item.url | prepend:site.baseurl | prepend:site.url}}"><img src = "{{site.url}}/{{site.baseurl}}/assets/img/{{ item.thumb}}" width = "200px" height = "200px"><p>{% if item.short_title %}{{ item.short_title }}{% else %}{{ item.title }}{% endif %}</p></a> </div>
  {% endif %}
{% endfor %}
</div>
