---
layout: page
title: Trauma & design
permalink: /trauma
comments: false
categories: trauma
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">

<h4>Key terms</h4>

{% assign termlist = site.data.terms | where_exp: "item", "item.categories contains page.categories" %}

{% for term in termlist %}

<div class="card">
  <h5 class="card-title">{{ term.name }}</h5>
  <p class="card-text">{{ term.definition }}</p>
</div>

{% endfor %}

<p>LINKS</p>

<p>LINKS</p>

<h4>Topic Area</h4>

<p>LINKS!</p>

</div>

</div>
