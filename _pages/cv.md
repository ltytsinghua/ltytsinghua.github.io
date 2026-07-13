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

Department of Physics, Tsinghua University, Beijing 100084, China<br>
Email: [lin-ty21@mails.tsinghua.edu.cn](mailto:lin-ty21@mails.tsinghua.edu.cn)

Education
======
* Ph.D. in Condensed Matter Theory, Department of Physics, Tsinghua University, 2021 – 2026 (expected)
* B.S. in Physics (Elite Program), Nanjing University, 2017 – 2021
* Northeast Yucai School (Gifted Education Program), 2012 – 2017

Research interests
======
* Phenomenological theory of unconventional superconductivity
* Frustrated spin systems
* Development of tensor-network algorithms

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
* First-Class Scholarship, Department of Physics, Tsinghua University, 2025
* Outstanding Graduate, Nanjing University, 2021
* First-Class Scholarship, Department of Physics, Nanjing University, 2019
