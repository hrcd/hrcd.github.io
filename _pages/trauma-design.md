---
title: Trauma & design
permalink: /trauma
comments: false
categories: trauma
---

# Key terms

The terms listed below are intentionally framed in plain language, or words that are commonly used in conversation. A wide range of disciplines contribute to, document, study, or ameliorate trauma, including: behavioral health, clinical psychology, decolonial studies, education, gender studies, indigenous studies, law, neurophysiology, positive psychology, public health, social justice, and wellness. Each discipline has specialist terms to describe various aspects of trauma; these are listed in the 'related terms' section below each main term.

{% assign termlist = site.data.terms | where_exp: "item", "item.categories contains page.categories" %}
{% assign introterms = site.data.terms | where_exp: "item", "item.tags contains 'intro'" %}
{% assign harms = site.data.terms | where: "tags", "harms" %}
{% assign helps = site.data.terms | where: "tags", "helps" %}
{% assign hrcd = site.data.terms | where: "tags", "hrcd" %}


## Trauma 101

*What do we talk about when we talk about trauma? Some of the commonly used terms, and our collective understandings of them.*

{% for term in introterms %}

<dl>
  <dt>{{ term.name | capitalize }}</dt>
  <dd>{{ term.definition }}

  {% if term.related != nil %}<br>
  <strong>Related terms:</strong> {{ term.related }}
  {% endif %}

  {% if term.people != nil %}<br>
  <strong>People doing work in this area:</strong> {{ term.people }}
  {% endif %}
  </dd>
</dl>

{% endfor %}

---
## Harms related to Trauma

*What are the negative associations with trauma? Our understandings of the origins of trauma, and harms or negative effects associated with it.*

{% for term in site.data.terms | where: "tags", "harms" %}

<dl>
  <dt>{{ term.name | capitalize  }}</dt>
  <dd>{{ term.definition }}

  {% if term.related != nil %}<br>
  <strong>Related terms:</strong> {{ term.related }}
  {% endif %}

  {% if term.people != nil %}<br>
  <strong>People doing pioneering related work:</strong> {{ term.people }}
  {% endif %}
  </dd>
</dl>

{% endfor %}

---
## Healing related to trauma

*What are the positive associations with trauma? Our understandings of the healthy and healing associations with trauma, and benefits arising from it.*

{% for term in site.data.terms | where: "tags", "helps" %}

<dl>
  <dt>{{ term.name | capitalize  }}</dt>
  <dd>{{ term.definition }}

  {% if term.related != nil %}<br>
  <strong>Related terms:</strong> {{ term.related }}
  {% endif %}

  {% if term.people != nil %}<br>
  <strong>People doing pioneering related work:</strong> {{ term.people }}
  {% endif %}
  </dd>
</dl>

{% endfor %}

---

## Trauma and human rights centered design

*How does human rights centered design relate to trauma? Our early thoughts on trauma as an intersectional term, and a lens through which to view human rights centered design work.*

{% for term in hrcd %}

<dl>
  <dt>{{ term.name | capitalize  }}</dt>
  <dd>{{ term.definition }}

  {% if term.related != nil %}<br>
  <strong>Related terms:</strong> {{ term.related }}
  {% endif %}

  {% if term.people != nil %}<br>
  <strong>People doing pioneering related work:</strong> {{ term.people }}
  {% endif %}
  </dd>
</dl>

{% endfor %}

---

## Trauma-related design initiatives

{% assign movements = site.data.movements | group_by: "type" %}
{% for type in movements  %}
<h4> {{ type.name | capitalize }} </h4>
  <ul>
    {% for movement in type.items %}
        <li><a href="{{ movement.link }}">{{ movement.name }}</a><br>
        <strong>Type:</strong> {{ movement.type | capitalize }} | <strong>Topics:</strong> {{ movement.categories | capitalize }}</li>
    {% endfor %}
  </ul>
{% endfor %}

---

## Trigger self-care and first aid
When a trigger is experienced, there are many strategies from a wide range of knowledge traditions that can assist a triggered person with regulating, and accelerate returning to a non-triggered state. Some of the ones listed below we have found personally helpful.

<ul>
  <li>jin shen point 17 - deactivates the vagus nerve</li>
  <li>3-4-5 breathing - stimulates the respiratory pacemaker in the brain</li>
  <li>orienting ("here we all are, safe together") - speeds reversal of amygdala hijack through combination of somatic experiencing and prefrontal reasoning.</li>
  <li>breath of fire - stimulates the respiratory pacemaker in the brain</li>
  <li>chanting</li>
  <li>therapeutic tremoring</li>
  <li>patting</li>
  <li>grounding</li>
  <li>high energy movement / dancing</li>
</ul>
