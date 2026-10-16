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
* **Ph.D. in Condensed Matter Theory (direct Ph.D.)**, Department of Physics, Tsinghua University, 2021 – 2027 (expected), advised by Prof. Guang-Ming Zhang
  * Researches tensor-network algorithms and phenomenological theories of unconventional superconductors. Four papers published in international journals, one submitted, and two manuscripts in preparation.
* **B.S. in Physics (Elite Program)**, Department of Physics, Nanjing University, 2017 – 2021; GPA: 4.40/5.0
  * Completed foundational university-level mathematics and physics courses; junior-year fall exchange in the Department of Physics at the University of California, Berkeley, GPA: 4.0/4.0.

Research profile
======
My research focuses on efficient computation and theoretical modeling of many-body physical systems. I develop tensor-network algorithms by improving network architectures and optimization methods, addressing convergence problems in complex-system calculations and improving computational efficiency and numerical stability. I also study physical phenomena in real unconventional superconducting materials, extracting key mechanisms from experimental results, building theoretical models, and predicting potential new phases. This work combines algorithm design, numerical computation, and mathematical modeling.

Publications
======
  <ul>{% assign pubs = site.publications | sort: "date" | reverse %}
  {% for post in pubs %}{% unless post.hide_meta == true %}
    {% include archive-single-cv.html %}
  {% endunless %}{% endfor %}
  {% for post in pubs %}{% if post.hide_meta == true %}
    {% include archive-single-cv.html %}
  {% endif %}{% endfor %}</ul>

Entrepreneurial experience
======
* **Duowei Youxue (Shenyang)**, Co-founder, 2026 – present
  * Co-founded a K–12 education organization and led teaching, curriculum development, and teacher recruitment; 100+ students and a 15-person teaching team.
  * Built an AI-assisted lecture-generation workflow with Claude Code: split textbook PDFs with PDFsam Basic, parsed them with MinerU, generated LaTeX lecture notes and Beamer slides, and converted them to WeChat public-account layouts. Used for middle- and high-school physics, physics competitions, and junior-high mathematics competition materials.
  * Used Claude Opus 5.5 and Manim to create visual K–12 teaching content, including dynamic geometry solutions and physics problem demonstrations; project ongoing.

Technical skills
======
* **Mathematics and physics:** linear algebra, statistical physics, and many-body physics
* **Computational methods:** tensor-network representations, tensor contraction, variational optimization, and tensor renormalization
* **Programming and AI tools:** Python, Claude Code, Codex, MinerU, PDFsam Basic, and Manim

Awards and honors
======
* First-Class Scholarship, Department of Physics, Tsinghua University, 2025
* Outstanding Graduate, Nanjing University, 2021
* First-Class Scholarship, Department of Physics, Nanjing University, 2019
