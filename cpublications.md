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


### Journal
{% for item in papers %}
{% if item.class == "journal" %}
* {{item.author}}, {% if item.doi %} [**"{{ item.title}}"**]({{item.doi}}), {% else %}"{{ item.title}}",{% endif %} *{{ item.venue}}*, {{item.year}}{% if item.preprint %}, ([Pre-print]({{site.url}}/{{site.baseurl}}/assets/pdf/{{item.preprint}})){% endif %}{% if item.arxiv %}, ([arXiv]({{item.arxiv}})){% endif %}.
{% endif %}
{% endfor %}


### Conference:
{% for item in papers %}
{% if item.class == "conf" %}
* {{item.author}}, {% if item.doi %} [**"{{ item.title}}"**]({{item.doi}}), {% else %}"{{ item.title}}",{% endif %} *{{ item.venue}}*, {{item.year}}{% if item.preprint %}, ([Pre-print]({{site.url}}/{{site.baseurl}}/assets/pdf/{{item.preprint}})){% endif %}{% if item.arxiv %}, ([arXiv]({{item.arxiv}})){% endif %}.
{% endif %}
{% endfor %}
