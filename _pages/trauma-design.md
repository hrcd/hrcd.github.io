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
{% assign introterms = site.data.terms | where_exp: "item", "item.tags contains 'intro'" %}
{% assign harms = site.data.terms | where: "tags", "harms" %}
{% assign helps = site.data.terms | where: "tags", "helps" %}
{% assign hrcd = site.data.terms | where: "tags", "hrcd" %}


<h5 id="101">Trauma 101</h5>
<p><em>What do we talk about when we talk about trauma? Some of the commonly used terms, and our collective understandings of them.</em></p>

{% for term in introterms %}

<dl>
  <dt>{{ term.name }}</dt>
  <dd>{{ term.definition }}

  {% if term.related != nil %}<br>
  <strong>Related terms:</strong> {{ term.related }}
  {% endif %}
  </dd>
</dl>

{% endfor %}

<hr>
<h5 id="harms">Harms related to Trauma</h5>
<p><em>What are the negative associations with trauma? Our understandings of the origins of trauma, and harms or negative effects associated with it.</em></p>

{% for term in harms %}

<dl>
  <dt>{{ term.name }}</dt>
  <dd>{{ term.definition }}

  {% if term.related != nil %}<br>
  <strong>Related terms:</strong> {{ term.related }}
  {% endif %}
  </dd>
</dl>

{% endfor %}

<hr>
<h5 id="harms">Healing related to trauma</h5>
<p><em>What are the positive associations with trauma? Our understandings of the healthy and healing associations with trauma, and benefits arising from it.</em></p>

{% for term in helps %}

<dl>
  <dt>{{ term.name }}</dt>
  <dd>{{ term.definition }}

  {% if term.related != nil %}<br>
  <strong>Related terms:</strong> {{ term.related }}
  {% endif %}
  </dd>
</dl>

{% endfor %}

<hr>
<h5 id="hrcd">Trauma and human rights centered design</h5>
<p><em>How does human rights centered design relate to trauma? Our early thoughts on trauma as an intersectional term, and a lens through which to view human rights centered design work.</em></p>

{% for term in hrcd %}

<dl>
  <dt>{{ term.name }}</dt>
  <dd>{{ term.definition }}

  {% if term.related != nil %}<br>
  <strong>Related terms:</strong> {{ term.related }}
  {% endif %}
  </dd>
</dl>

{% endfor %}


<h4 id="init">Trauma-related design initiatives</h4>

{% assign movements = site.data.movements | group_by: "type" %}
{% for type in movements  %}
<h5> {{ type.name | capitalize }} </h5>
  <ul>
    {% for item in type.items %}
        <li><a href="{{ movement.link }}">{{ movement.name }}</a><br>
        Type: {{ movement.type | capitalize }} | Topics: {{ movement.categories | capitalize }}</li>
    {% endfor %}
  </ul>
{% endfor %}


{% for movement in site.data.movements %}
  <ul>
      <li><a href="{{ movement.link }}">{{ movement.name }}</a><br>
      Type: {{ movement.type | capitalize }} | Topics: {{ movement.categories }}</li>
  </ul>
{% endfor %}


</div>

</div>
