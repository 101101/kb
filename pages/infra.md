---
layout: page
title: Infra
permalink: /infra/
---

# Infra

{% if user %}
  Hello {{ user.name }}!
{% endif %}

Welcome to the {{ site.title }} Infra pages! Here you can quickly jump to a 
particular page.

---

<div class="section-index">
    <hr class="panel-line">
    {% for post in site.docs %}
        {% if post.category contains "infra" %}
            <div class="entry">
            <h5><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h5>
            <p>{{ post.description }}</p>
            </div>
        {% endif %}
    {% endfor %}
</div>

---
