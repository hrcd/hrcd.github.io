---
layout: page
title: Trauma & design
permalink: /trauma
comments: false
categories: trauma
---

<div class="row justify-content-between">
<div class="col-md-8 pr-5">

#### Key terms

{% assign termlist = site.data.terms | where_exp: "item", "item.categories contains page.categories" %}

{% for term in termlist %}
  <h5>{{ term.name }}</h5>
  <p>{{ term.description }}</p>

{% endfor %}

<p>LINKS</p>

<p>LINKS</p>

<h4>Topic Area</h4>

<p>LINKS!</p>

</div>

</div>
