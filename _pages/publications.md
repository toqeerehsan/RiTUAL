---
title: "RiTUAL - Publications"
layout: gridlay
excerpt: "RiTUAL -- Publications."
sitemap: false
permalink: /publications/
---

<h3>Publications</h3>

<!--
Jump to [Under Review Articles](#under-review-articles), [Patents](#patents), [List of All Publications](#list-of-all-publications).

<h4 id="under-review-articles"> Under Review Articles </h4>

{% for publi in site.data.under_review %}

  <span class="navy">{{ publi.title }}</span><br />
  <em>{{ publi.authors }} </em><br />
  In: {{ publi.publisher }}, <i>(Submission Date: {{publi.date}})</i>
<div class="row" style="margin-bottom:5px;padding-bottom:0px">
  <div class="col-sm-12 clearfix">
  <a class="small-sky-btn" data-toggle="collapse" href="#abs-{{ forloop.index }}" role="button" aria-expanded="false" aria-controls="abs-{{ forloop.index }}">
    Abstract
  </a>
</div>
</div>
<div class="collapse" id="abs-{{ forloop.index }}">
    {{publi.abs}}
</div>

{% endfor %}

<h4 id="patents"> Patents </h4>

{% for i in site.data.patents %}

  {{ i.title }} <br />
  <em>{{ i.authors }} </em><br />
  <span class="sky">{{ i.patent-id }}</span>

{% endfor %}

<h4 id="list-of-all-publications"> List of all Publications </h4>   -->

{% for publi in site.data.publist %}

  <span class="gray bold">{{ publi.title }}</span><br /> 
  <em>{{ publi.authors }} </em><br />
  In: {{publi.publisher}}, <i>(Publication Date: {{ publi.date }})</i>
<div class="row" style="margin-bottom:1px;padding-bottom:0px">
  <div class="col-sm-12 clearfix">
  <a class=".small-sky-btn" data-toggle="collapse" href="#abstract-{{ forloop.index }}" role="button" aria-expanded="false" aria-controls="abstract-{{ forloop.index }}">
  Abstract
  </a>
  <a class=".small-sky-btn" href="{{ publi.url }}" target="_blank">
    URL
  </a>
  <a class=".small-sky-btn" data-toggle="collapse" href="#bibtex-{{ forloop.index }}" role="button" aria-expanded="false" aria-controls="bibtex-{{ forloop.index }}">
    BibTeX
  </a>
</div>
</div>

<div class="collapse collapse_font" id="abstract-{{ forloop.index }}">
    {{publi.abs}}
</div>

<div class="collapse collapse_font" id="bibtex-{{ forloop.index }}">
   <pre>{{publi.bibtex}}</pre>
</div>
{% endfor %}