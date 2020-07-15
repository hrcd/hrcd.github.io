---
layout: page
title: Trauma & design
permalink: /trauma
comments: false
categories: trauma
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">

<h4 id="terms">Key terms</h4>

{% assign termlist = site.data.terms | where_exp: "item", "item.categories contains page.categories" %}
{% assign 101 = site.data.terms | where: "tags", "101" %}
{% assign harms = site.data.terms | where: "tags", "harms" %}
{% assign helps = site.data.terms | where: "tags", "helps" %}
{% assign hrcd = site.data.terms | where: "tags", "hrcd" %}

{% for term in termlist %}

  <h6>{{ term.name }}</h5>
  <p>{{ term.definition }}</p>

{% endfor %}


<h5 id="101">Trauma 101</h4>

{% for term in 101 %}

  <h5 >{{ term.name }}</h5>
  <p >{{ term.definition }}</p>

{% endfor %}


<h4 id="init">Trauma-related design initiatives</h4>

{% assign movements = site.data.movements %}

{% for movement in movements %}

  <h5 >{{ term.name }}</h5>
  <p >{{ term.definition }}</p>

{% endfor %}

</div>

</div>
