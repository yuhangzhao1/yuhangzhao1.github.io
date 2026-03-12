---
layout: page
permalink: /people/
title: MadAbility Lab
description: members of the lab or group
nav: true
nav_order: 8
horizontal: false
---

<!-- pages/people.md -->
I lead the [madAbility Lab](https://madability.cs.wisc.edu/) and have the privilege to work with many talented students and collaborators.

<br>
{% assign sorted_people = site.people | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-2">
    {% for people in sorted_people %}
      {% include people_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
{% else %}
  <div class="grid">
    {% for people in sorted_people %}
      {% include people.liquid %}
    {% endfor %}
  </div>
{% endif %}
