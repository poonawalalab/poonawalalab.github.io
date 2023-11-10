---
layout: research
title: Research
permalink: /research/
---

## Research Overview

Our lab works on developing theory and technologies for robot control. We extend traditional robot control design methods by incorporating machine learning using systematic approaches. We emphasize learning-based control strategies that are provably correct. Our members acquire expertise in topics from control systems, robotics, optimization, and machine learning. We currently focus on the following areas:
1. Contact-rich manipulation
1. Verification of learned neural network controllers
1. Navigation without localization

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
