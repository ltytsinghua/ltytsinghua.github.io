---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* Ph.D. in Physics (Condensed Matter Theory), Tsinghua University, expected <!-- YEAR -->
* B.S. in Physics, <!-- UNIVERSITY -->, <!-- YEAR -->

Research experience
======
<!-- TODO: list research positions, e.g. -->
<!-- * YEAR–YEAR: Research topic / group -->
<!--   * Institution -->
<!--   * Advisor: -->

Research interests
======
* Tensor networks
* Statistical mechanics
* Superconductivity
* Frustrated magnetism

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Awards and honors
======
<!-- TODO: list awards -->

Service
======
<!-- TODO: list service / reviewing / organizing -->
