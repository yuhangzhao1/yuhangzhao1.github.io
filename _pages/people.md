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

<h2>Graduate Students</h2>
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
