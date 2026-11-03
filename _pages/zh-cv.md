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

<p><a class="btn btn--primary" href="{{ base_path }}/files/cv_zh.pdf" download>下载 CV PDF</a></p>

清华大学物理系，北京 100084<br>
邮箱：[lin-ty21@mails.tsinghua.edu.cn](mailto:lin-ty21@mails.tsinghua.edu.cn)

教育经历
======
* **清华大学物理系凝聚态理论专业博士（直博）**，2021 – 2026.12（预计），导师：张广铭教授
* **南京大学物理系拔尖班本科**，2017 – 2021
* **加州大学伯克利分校物理系交换生**，2019.8 – 2019.12

求职意向
======
AI for Physics、Physics for AI。

研究兴趣
======
**当前研究方向**

* **张量网络方法**：发展统计物理问题中的张量网络方法。
* **阻挫磁性系统**：研究阻挫磁性系统中的新奇磁有序相及相变。
* **非常规超导体的唯象理论**：关注超导材料中的非常规涡旋激发，如分数涡旋激发。

**未来研究方向**

* **Physics for AI**：提升 AI 的推理能力与物理能力，研究 AI 的可解释性。
* **AI for Science**：利用 AI 加速物理学发现。

发表论文
======
  <ul>{% assign pubs = site.publications | sort: "date" | reverse %}
  {% for post in pubs %}{% unless post.hide_meta == true %}
    {% include archive-single-cv.html %}
  {% endunless %}{% endfor %}
  {% for post in pubs %}{% if post.hide_meta == true %}
    {% include archive-single-cv.html %}
  {% endif %}{% endfor %}</ul>

获奖荣誉
======
* 清华大学物理系一等奖学金，2025，2026
* 南京大学优秀毕业生，2021
* 南京大学物理系一等奖学金，2019
