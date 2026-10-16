---
layout: archive
title: "简历"
permalink: /zh/cv/
author_profile: true
lang: zh
locale: zh-CN
lang_alt_url: /cv/
lang_alt_label: "EN"
---

{% include base_path %}

<p><a class="btn btn--primary" href="{{ base_path }}/files/cv.pdf" download>下载 CV PDF</a></p>

清华大学物理系，北京 100084<br>
邮箱：[lin-ty21@mails.tsinghua.edu.cn](mailto:lin-ty21@mails.tsinghua.edu.cn)

教育经历
======
* **清华大学物理系凝聚态理论专业博士（直博）**，2021 – 2027（预计），导师：张广铭教授
  * 从事张量网络算法与非常规超导体的唯象理论相关研究，已在国际期刊发表四篇文章，另有一篇在投，两篇工作撰写中。
* **南京大学物理系拔尖班理学学士**，2017 – 2021，GPA 4.40/5.0
  * 系统学习大学数学与物理基础课程；大三上赴加州大学伯克利分校物理系交换，GPA 4.0/4.0。

求职意向
======
大模型训练、推理与新型 AI 范式探索。

研究概述
======
研究聚焦于多体物理系统的高效计算与理论建模，主要开展两方面工作：一是研究张量网络算法，通过改进张量网络的结构设计与优化方法，解决复杂物理系统计算中的算法不收敛问题，提升计算效率与数值稳定性；二是研究真实非常规超导材料中的物理现象，从实验结果中提炼关键物理机制，构建理论模型并预测潜在的新型物态。相关工作综合运用了算法设计、数值计算和数学建模方法。

发表论文
======
  <ul>{% assign pubs = site.publications | sort: "date" | reverse %}
  {% for post in pubs %}{% unless post.hide_meta == true %}
    {% include archive-single-cv.html %}
  {% endunless %}{% endfor %}
  {% for post in pubs %}{% if post.hide_meta == true %}
    {% include archive-single-cv.html %}
  {% endif %}{% endfor %}</ul>

创业经历
======
* **多维优学（沈阳）**，联合创始人，2026 – 至今
  * 联合创办 K12 教培机构，负责教学、课程研发与教师招聘；学生规模 100+ 人，教师团队 15 人。
  * 基于 Claude Code 搭建 AI 自动化讲义生成工作流：利用 PDFsam Basic 分割 PDF，用 MinerU 解析教材 PDF，自动生成 LaTeX 讲义与 Beamer 课件，并一键转换为公众号排版；已用于制作初高中课内物理、竞赛物理及初中数学竞赛讲义，形成完整的课程体系。
  * 用 Claude Opus 5.5 + Manim 制作 K12 教学内容可视化（几何题动态解答、物理题目过程演示），项目进行中。

专业技能
======
* **数理基础：**线性代数、统计物理、多体物理
* **计算方法：**张量网络表示、张量运算与收缩、变分优化、张量重整化群
* **编程与 AI 工具：**Python、Claude Code、Codex、MinerU、PDFsam Basic、Manim

获奖荣誉
======
* 清华大学物理系一等奖学金，2025
* 南京大学优秀毕业生，2021
* 南京大学物理系一等奖学金，2019
