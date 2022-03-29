---
layout: page
title: Teaching
permalink: /teaching/
---
## Courses:
<!-- <div class = "flex-container"> -->
{% for item in site.courses %}
1. <a href="{{ item.url | prepend:site.baseurl | prepend:site.url}}"> {{ item.title }} </a>
{% endfor %}
<!-- </div> -->
