---
layout: research
title: Research
permalink: /research/
---

## Research Overview
<div class = "justified">
<p>Our lab works on developing theory and technologies for robot control. Our members acquire expertise in topics from control systems, robotics, optimization, and machine learning. We focus on the following two themes.</p></div>
<ul>
<li><h4> Learning For Control</h4><div class = "justified"><p>Traditional methods for robot control rely on hard-coded abilities, so that their high performance is only achieved in controlled laboratory and factory settings. Our lab extends traditional robot control design methods by incorporating machine learning using systematic approaches.</p> 
<p>We emphasize learning-based control strategies that are provably correct. We rigorously and systematically account for uncertainties and limitations of machine learning techniques in the control design. This approach involves applying principles from control, dynamics, and learning from data to our problems. This control-theory-aware approach leads to smaller models trained using less data without sacrificing performance.</p>
Two examples of what we do:
<ul>
<li> Path-following / Lane-keeping using direct sensor feedback (no SLAM) and a support vector machine.</li>
<li> Fully automated control synthesis for (learned)  dynamics neural network models.</li>
</ul>
</div></li>
<li><h4>>Distributed Controllers</h4><div class = "justified"><p>Our lab explores decentralized or distributed controller designs and implementations that enable robust motion control of robots.
Controllers implemented on centralized computers with sequential program execution are not robust. Communicating control commands to actuators is also an issue for the latter. We apply principles from multi-agent control and networked control systems to design robust distributed control algorithms and architectures.</p></div></li>
</ul>


<h2>Research Projects</h2>

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