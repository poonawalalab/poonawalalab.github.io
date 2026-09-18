---
layout: page
title: Publications
permalink: /publications/
---
{% assign papers = site.papers | sort: 'date' | reverse %}

### Pre-prints
{% for item in papers %}
{% if item.class == "pre" %}
* {{item.author}}, {% if item.doi %} [**"{{ item.title}}"**]({{item.doi}}), {% else %}"{{ item.title}}",{% endif %} *{{ item.venue}}*, {{item.year}}{% if item.preprint %}, ([Pre-print]({{site.url}}/{{site.baseurl}}/assets/pdf/{{item.preprint}})){% endif %}{% if item.arxiv %}, ([arXiv]({{item.arxiv}})){% endif %}.
{% endif %}
{% endfor %}


### Under Review

{% for item in papers %}
{% if item.class == "sub" %}
* {{item.author}}, {% if item.doi %} [**"{{ item.title}}"**]({{item.doi}}), {% else %}"{{ item.title}}",{% endif %} *{{ item.venue}}*, {{item.year}}{% if item.preprint %}, ([Pre-print]({{site.url}}/{{site.baseurl}}/assets/pdf/{{item.preprint}})){% endif %}{% if item.arxiv %}, ([arXiv]({{item.arxiv}})){% endif %}.
{% endif %}
{% endfor %}

### Published
{% assign paper_classes = "journal,conf" | split: "," %}
{% for item in papers %}
{% if paper_classes contains item.class and item.year >= 2018 %}
* **[{{ item.year }} {{ item.class | capitalize }}]** {{item.author}}, {% if item.doi %} [**"{{ item.title}}"**]({{item.doi}}), {% else %}"{{ item.title}}",{% endif %} *{{ item.venue}}*, {{item.year}}{% if item.preprint %}, ([Pre-print]({{site.url}}/{{site.baseurl}}/assets/pdf/{{item.preprint}})){% endif %}{% if item.arxiv %}, ([arXiv]({{item.arxiv}})){% endif %}.
{% endif %}
{% endfor %}

