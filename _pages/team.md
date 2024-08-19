---
title: "RiTUAL - Team"
layout: gridlay
excerpt: "RiTUAL: Team members"
sitemap: false
permalink: /team/
---

<h3>Group Members</h3>

<!--Jump to [staff](#staff), [master and bachelor students](#master-and-bachelor-students), [alumni](#alumni), [administrative support](#administrative-support). -->
Jump to [postdocs](#postdocs), [doctoral students](#doctoral-students), [RAs](#research-assistants), [master students](#master-and-bachelor-students), [alumni](#alumni), [administrative support](#administrative-support).

<h4 id="staff">Group Leader</h4>
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-12 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/mbzuai_staff/{{ member.photo }}" class="img-responsive" width="30%" style="float: left" />
  <p class="sub-heading bold">{{ member.name }}</p>
  <i class="gray">{{ member.info }}</i>

[//]: # (  <a href="mailto:{{ member.email }}">{{ member.email }}</a>)
  <div style="text-align: justify;">
  <p>Professor Solorio’s research focuses on information extraction (structured prediction) problems, multilingual models, with a special emphasis on mixed language settings, low resource NLP, and more recently, multimodal content understanding.</p>
  </div>

  <h5>Education:</h5>
<ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 | markdownify}} </li>
  <li> {{ member.education2 | markdownify}} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  {% if member.number_educ == 5 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  <li> {{ member.education5 }} </li>
  {% endif %}

</ul>
</div>
<div class="col-sm-12 clearfix">
  <a href="{{ member.website }}" class="custom-sky-btn" target="_blank">PERSONAL WEBSITE</a>
  <a href="{{ member.google_scholar }}" class="custom-sky-btn" target="_blank">GOOGLE SCHOLAR</a><br>
</div>


{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


<h4 id="postdocs">Postdocs</h4>

<h4 id="doctoral-students">Doctoral Students</h4>

<h4 id="research-assistants">Research Assistants</h4>

<h4 id="master-and-bachelor-students">Master Students</h4>
{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <p class="sub-heading">{{ member.name }}</p>
  <i>{{ member.info }} <!-- <br>email: <{{ member.email }}></i> -->
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

  {% if member.number_educ == 4 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


<h4 id="alumni">Alumni</h4>

{% assign number_printed = 0 %}
{% for member in site.data.alumni_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <p class="sub-heading">{{ member.name }}</p>
  <i>{{ member.duration }} <br> Role: {{ member.info }}</i>
  <ul style="overflow: hidden">

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<h4 id="Former visitors, BSc/ MSc students">Former Visitors, BSc/ MSc Students</h4>
<div class="row">

<div class="col-sm-4 clearfix">
<p class="sub-heading">Visitors</p>
{% for member in site.data.alumni_visitors %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<p class="sub-heading">Master students</p>
{% for member in site.data.alumni_msc %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<p class="sub-heading">Bachelor Students</p>
{% for member in site.data.alumni_bsc %}
{{ member.name }}
{% endfor %}
</div>

</div>


<h4 id="administrative-support">Administrative Support</h4>
<a href="mailto:Rijsewijk@Physics.LeidenUniv.nl">Ellie van Rijsewijk</a> is helping us (and other groups) with administration.
