---
layout: research
title: People
permalink: /people/
---
See  <a href="{{site.baseurl | prepend:site.url}}/people/#labopenings"> below </a> for openings.> 


<h3>Principal Investigator:</h3>
<div class = "flex-container">
{% for item in site.profiles %}
{% if item.position == "PI" %}
  <div class = "thumby"><a href="{{ item.url | prepend:site.baseurl | prepend:site.url}}"><img src = "{{site.url}}/{{site.baseurl}}/assets/img/{{ item.thumb}}" width = "170px" height = "170px"><p>{{ item.title }}</p></a> </div>
  {% endif %}
{% endfor %}
</div>


<h3>Ph.D Researchers:</h3>
<div class = "flex-container">
{% for item in site.profiles %}
{% if item.position == "phd" %}
  {% if item.status == "active" %}
  <div class = "thumby"><a href="{{ item.url | prepend:site.baseurl | prepend:site.url}}"><img src = "{{site.url}}/{{site.baseurl}}/assets/img/{{ item.thumb}}" width = "170px" height = "170px"><p>{{ item.title }}</p></a> </div>
  {% endif %}
{% endif %}  
{% endfor %}
</div>

<h3>MS Researchers:</h3>
<div class = "flex-container">
{% for item in site.profiles %}
{% if item.position == "ms" %}
  {% if item.status == "active" %}
  <div class = "thumby"><a href="{{ item.url | prepend:site.baseurl | prepend:site.url}}"><img src = "{{site.url}}/{{site.baseurl}}/assets/img/{{ item.thumb}}" width = "170px" height = "170px"><p>{{ item.title }}</p></a> </div>
  {% endif %}
{% endif %}  
{% endfor %}
</div>

<h3>Undergraduate Researchers:</h3>
<div class = "flex-container">
{% for item in site.profiles %}
{% if item.position == "bs" %}
  {% if item.status == "active" %}
  <div class = "thumby"><a href="{{ item.url | prepend:site.baseurl | prepend:site.url}}"><img src = "{{site.url}}/{{site.baseurl}}/assets/img/{{ item.thumb}}" width = "170px" height = "170px"><p>{{ item.title }}</p></a> </div>
  {% endif %}
{% endif %}  
{% endfor %}
</div>

<h3>High-School Researchers:</h3>
<div class = "flex-container">
{% for item in site.profiles %}
{% if item.position == "hs" %}
  {% if item.status == "active" %}
  <div class = "thumby"><a href="{{ item.url | prepend:site.baseurl | prepend:site.url}}"><img src = "{{site.url}}/{{site.baseurl}}/assets/img/{{ item.thumb}}" width = "170px" height = "170px"><p>{{ item.title }}</p></a> </div>
  {% endif %}
{% endif %}  
{% endfor %}
</div>

<h3>Alumni:</h3>
<div class = "flex-container">
<ul>
{% for item in site.profiles %}
{% if item.position != "PI" %}
  {% if item.status == "alumnus" or item.status == "alum" %}
  <!--div class = "thumby"><a href="{{ item.url | prepend:site.baseurl | prepend:site.url}}"><img src = "{{ item.thumb}}" width = "170px" height = "170px"><p>{{ item.title }}</p></a> </div-->
  <div><li> {{item.title}} </li> </div>
  {% endif %}
{% endif %}  
{% endfor %}
</ul>
</div>


<!-- <div id="labopenings"> -->
<!-- <h3> Research Opportunities </h3> -->
<!-- The lab is looking for a research assistant to work on computational control for contact-rich manipulation. The project will implement motion planning algorithms for finding multi-contact paths in the configuration space of a robot-object system, and computational control algorithms based on optimization to find stabilizing controllers for those paths. The project will need strong coding skills and comfort with mathematical optimization. --> 

<!-- Ideal candidates have experience implementing convex optimization problems in code and motion planning algorithms like RRT*. They will also know how to avoid implementing algorithms inefficiently. -->

<!-- To apply for this opening, send an <a href="mailto:hasan.poonawala@uky.edu"> email </a> to Hasan Poonawala with -->
<!-- <ul> -->
<!-- <li> a one-page resume, </li> -->
<!-- <li> up to two papers or technical reports primarily written by you, and </li> -->
<!-- <li> a transcript. </li> -->
<!-- </ul> -->
<!-- <p>
Preference will be given to candidates with strong records in research/coursework related to mathematics, optimization, control, or robotics. Individuals with significant theoretical or experimental experience are encouraged to apply.</p>
<p>
<h4>Funding opportunities:</h4>
The lab has support for Ph.D studies beginning Fall 2020, in the form of Research and Teaching Assistantships. Apply as above.</p> --->
<!-- </div> -->
