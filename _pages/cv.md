---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
lang: en
lang_alt_url: /zh/cv/
lang_alt_label: "中文"
redirect_from:
  - /resume
---

{% include base_path %}

<p><a class="btn btn--primary" href="{{ base_path }}/files/cv.pdf" download>Download CV as PDF</a></p>

Department of Physics, Tsinghua University, Beijing 100084, China<br>
Email: [lin-ty21@mails.tsinghua.edu.cn](mailto:lin-ty21@mails.tsinghua.edu.cn)

Education
======
* **Ph.D. in Physics (Condensed Matter Theory)**, Department of Physics, Tsinghua University, 2021 – 2026.12 (expected), advised by Prof. Guang-Ming Zhang
* **B.S. in Physics, Top-notch Undergraduate Program**, Department of Physics, Nanjing University, 2017 – 2021
* **Exchange Student**, Department of Physics, University of California, Berkeley, 2019.8 – 2019.12
* **Middle & High School, Gifted Education Program**, Northeast Yucai School, Shenyang, 2012.9 – 2017.6

Objective
======
AI for Physics, Physics for AI.

Research interests
======
**Current**

* **Tensor-network methods:** developing tensor-network methods for problems in statistical physics.
* **Frustrated magnetism:** exotic magnetic orders and phase transitions in frustrated magnetic systems.
* **Phenomenology of unconventional superconductors:** unconventional vortex excitations in superconductors, such as fractional vortices.

**Future**

* **Physics for AI:** improving the reasoning and physics capabilities of AI, and studying AI interpretability.
* **AI for Science:** using AI to accelerate discovery in physics.

Publications
======
  <ul>{% assign pubs = site.publications | sort: "date" | reverse %}
  {% for post in pubs %}{% unless post.hide_meta == true %}
    {% include archive-single-cv.html %}
  {% endunless %}{% endfor %}
  {% for post in pubs %}{% if post.hide_meta == true %}
    {% include archive-single-cv.html %}
  {% endif %}{% endfor %}</ul>

Awards and honors
======
* First-Class Scholarship, Department of Physics, Tsinghua University, 2025, 2026
* Outstanding Graduate, Nanjing University, 2021
* First-Class Scholarship, Department of Physics, Nanjing University, 2019
