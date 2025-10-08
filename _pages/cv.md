---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

<!-- markdownlint-disable MD033 -->

{% include base_path %}

---

<div style="display: flex; justify-content: space-between;">
  <div>
    Phone (China): <a href="tel:+8613706267747" target="_blank">+86 13706267747</a><br>
    Phone (US): <a href="tel:+19192014521" target="_blank">+1 919-201-4521</a>
  </div>
  <div>
    Email: <a href="mailto:jw853@duke.edu" target="_blank">jw853@duke.edu</a><br>
    Website: <a href="https://www.qqgjyx.com" target="_blank">www.qqgjyx.com</a>
  </div>
  <div style="text-align: center; margin-bottom: 20px;" class="no-print">
    <a href="{{ site.baseurl }}/files/resume.pdf" class="btn btn-primary" target="_blank" rel="noopener">
      <i class="fas fa-file-pdf" aria-hidden="true" style="margin-right:0.5em;"></i>
      PDF Resume
    </a>
    <style>
      .btn.btn-primary {
        background: #0d6efd;
        color: #fff;
        padding: 0.5em 1.5em;
        border-radius: 0.375rem;
        font-size: 1em;
        text-decoration: none;
        border: none;
        display: inline-flex;
        align-items: center;
        gap: 0.5em;
        cursor: pointer;
      }
      .btn.btn-primary:hover { background: #0a58ca; }
    </style>
  </div>
</div>

## EDUCATION

---

<div style="display: flex; justify-content: space-between;">
  <div>
    <strong>Duke Kunshan University (DKU) & Duke University Dual Degree</strong><br>
    <em>B.S. in Applied Math & Computational Science; Computer Science Track (DKU)</em><br>
    <em>B.S. in Interdisciplinary Studies; Applied Math & Computational Science; Computer Science (Duke)</em><br>
  </div>
  <div style="text-align: right;">
    Class of 2026<br>
    Kunshan, China<br>
    Durham, NC
  </div>
</div>
<div style="margin-top: -0.7em;"></div>
- GPA: 3.8/4.0; Dean's List with Distinction (24FA, 24SP), Dean's List (23FA)
- Courses: Deep Learning (A+), Machine Learning (A+), Matrix/Graph/Network Analysis (A+), Databases (A+), etc. <!-- Comp Science (A+), Calculus (A+), Biology (A+) -->
- Service/activities: Supported classmates at Duke as Kunshan Student Orientation Peer; Led weekly training sessions as Kendo Club Training Leader...

## HONORS & AWARDS

---

<div style="display: flex; justify-content: space-between;">
  <div>
    <strong><a href="https://www.kaggle.com/competitions/stanford-rna-3d-folding" target="_blank" rel="noopener">
      Stanford RNA 3D Folding (Kaggle)
    </a></strong><br>
    <em>Bronze Medal (Top 8%, 1500+ teams)</em>
  </div>
  <div style="text-align: right;">
    Feb 2025 - Sep 2025<br>
    Online
  </div>
</div>

## PROJECTS

---

**[qqgjyx.com/mheatmap](https://qqgjyx.com/mheatmap)**
[![GitHub stars](https://img.shields.io/github/stars/qqgjyx/mheatmap)](https://github.com/qqgjyx/mheatmap/stargazers)
<div style="margin-top: -0.7em;"></div>
- Developed a Python package for proportional heatmap visualization and spectral reordering, well-received by the community (600+ GitHub stars).
- Adopted by research groups and cited in multiple academic papers.

**[qqgjyx.com/pysgtsnepi](https://qqgjyx.com/pysgtsnepi)**
[![GitHub stars](https://img.shields.io/github/stars/qqgjyx/pysgtsnepi)](https://github.com/qqgjyx/pysgtsnepi/stargazers)
<div style="margin-top: -0.7em;"></div>
- Implemented the [SG-t-SNE-Π algorithm](https://t-sne-pi.cs.duke.edu/) in Python from scratch, making state-of-the-art dimension reduction more accessible to researchers.
- Improved ease of integration for data scientists by providing clean, well-documented APIs.

## PUBLICATIONS

---

<div style="margin-top: -1em;"></div>
<ul>{% for post in site.publications reversed %}
  <div style="margin-top: -1em;"></div>
  {% include archive-single-cv.html %}
{% endfor %}</ul>

## RESEARCH EXPERIENCE

---

<div style="display: flex; justify-content: space-between;">
  <div>
    <strong>Unsupervised/semi-supervised methods for biomedical tasks</strong><br>
    <em>Signature Work</em>; Research Assistant. PI: <a href="https://sites.google.com/site/shixinxupage/" target="_blank">Prof. Shixin Xu</a><br>
  </div>
  <div style="text-align: right;">
    Mar 2024 - Present<br>
    Kunshan, China
  </div>
</div>
<div style="margin-top: -0.7em;"></div>
- Researched on topics like 16S rRNA for bacterial culture media prediction and acute ischemic stroke reperfusion decision-making, etc.
- Utilized techniques like clustering, neural networks, ordinary differential equations to solve real-world problems; Developed novel models.
- Produced 2 conference papers and 1 thesis.

<div style="display: flex; justify-content: space-between;">
  <div>
    <strong>Classifying vigilance states in mouse EEG/EMG data</strong><br>
    <em>Summer Research Scholar</em>. PI: <a href="https://faculty.dukekunshan.edu.cn/faculty_profiles/shu-kit-eric-tam" target="_blank">Prof. Shu Kit Eric Tam</a> & <a href="https://faculty.dukekunshan.edu.cn/faculty_profiles/sze-chai-kwok" target="_blank">Prof. Sze Chai Kwok</a><br>
  </div>
  <div style="text-align: right;">
    Mar 2025 - Aug 2025<br>
    Kunshan, China
  </div>
</div>
<div style="margin-top: -0.7em;"></div>
- Studied how the Martian photoperiod affects the mammalian circadian system and sleep/wake patterns in mice and methods for vigilance state classification.
- Implemented a convolutional neural network to classify vigilance states using mouse electroencephalography (EEG) and electromyography (EMG) data.
- Produced 1 conference paper and 1 journal article.

<div style="display: flex; justify-content: space-between;">
  <div>
    <strong>Unsupervised segmentation in hyperspectral imaging</strong><br>
    <em>Summer Research</em>; Independent Study. PI: <a href="https://nicholas.duke.edu/people/staff/floros" target="_blank">Dimitrios Floros</a>, <a href="https://scholars.duke.edu/person/nikos.p.pitsianis" target="_blank">Prof. Nikos Pitsianis</a> & <a href="https://scholars.duke.edu/person/xiaobai.sun" target="_blank">Prof. Xiaobai Sun</a><br>
  </div>
  <div style="text-align: right;">
    Jun 2024 - Dec 2024<br>
    Durham, NC
  </div>
</div>
<div style="margin-top: -0.7em;"></div>
- Studied precursor clustering/community detection methods, and applied them to hyperspectral imaging. Collected >5 methods and >10 datasets.
- Utilized tools like Python (sklearn), MATLAB, Julia and techniques like k-nearest neighbor graph,  [Stochastic Graph t-SNE](https://t-sne-pi.cs.duke.edu/) and [Parallel Clustering with Resolution Variation](https://ieeexplore.ieee.org/document/10363552/) in the study.
- Developed python packages [mheatmap](https://qqgjyx.com/mheatmap) and [pysgtsnepi](https://qqgjyx.com/pysgtsnepi) aiding post and pre-processing of HSI data, well-received by the community (600+ GitHub stars).

<div style="display: flex; justify-content: space-between;">
  <div>
    <strong>Photon & exciton dynamics, photoluminescence, and superconductivity</strong><br>
    <em>Research Independent Study</em>. PI: <a href="https://faculty.dukekunshan.edu.cn/faculty_profiles/xiawa-wang" target="_blank">Prof. Xiawa Wang</a><br>
  </div>
  <div style="text-align: right;">
    Jan 2024 - May 2024<br>
    Kunshan, China
  </div>
</div>
<div style="margin-top: -0.7em;"></div>
- Researched on topics like temperature-induced electronic, magnetic, and structural properties in solid-state materials including Pb$$_{10-x}$$Cu$$_x$$(PO$$_4$$)$$_6$$O$$_3$$ (LK-99), KBaLnB$$_2$$O$$_6$$ (Ln=Gd,Yb,Tb), etc.
- Utilized tools like temperature-dependent X-ray diffraction, Raman spectroscopy, and density functional theory (DFT) calculations to study photoluminescence, phase transitions and ferromagnetism in these trending or rare-earth materials.
- Produced 1 conference paper.

## SKILLS

---

**Programming & Analysis:** Python, R, MATLAB, Julia, Wolfram, Java, C/C++, C#, Bash  
**Data & Web:** PostgreSQL, MongoDB, HTML/CSS, Cloudflare  
**Tools:** LaTeX, Markdown, Unity, Generative AI tools (e.g., Cursor, Stable Diffusion)  
**Languages:** English (Fluent), Mandarin (Native), Japanese, French

## TEACHING

---

{% for post in site.teaching reversed %}
  <p>{% include archive-single-CUSTOM-cv.html %}</p>
{% endfor %}

## WORK EXPERIENCE

---

<div style="display: flex; justify-content: space-between;">
  <div>
    <strong>Resident Assistant</strong><br>
    <em>Res Life, DKU</em>
  </div>
  <div style="text-align: right;">
    Aug 2024 - Present<br>
    Kunshan, China
  </div>
</div>
<div style="margin-top: -0.7em;"></div>
- Helped student residents with academic and personal issues, catalyzed an engaging community.
- Handled 50+ incidents; served 3 years.
- Wrote a Python script scraping Reddit images and resident roster for automatic door decoration creation, used by peer RAs.

<div style="display: flex; justify-content: space-between;">
  <div>
    <strong>Product Analyst, Intern</strong><br>
    <em>Second DX Division, NTT Data</em>
  </div>
  <div style="text-align: right;">
    Jul 2023 - Aug 2023<br>
    Wuxi, China
  </div>
</div>
<div style="margin-top: -0.7em;"></div>
- Assisted in development (backend) and the literature review on topics like LLMs, agentic systems, etc.
- Authored a professional report on software-related industries in China, focused on AI innovation.

<div style="display: flex; justify-content: space-between;">
  <div>
    <strong>Banker, Intern</strong><br>
    <em>Business Department, Bank of Huaxia</em>
  </div>
  <div style="text-align: right;">
    Jun 2023 - Jul 2023<br>
    Kunshan, China
  </div>
</div>
<div style="margin-top: -0.7em;"></div>
- Assisted in investigating the client business, including credit analysis, market research, etc.
- Drafted 50+ audit reports on local electronic enterprises, conducted in-depth industry research.

<!-- <div style="display: flex; justify-content: space-between;">
  <div>
    <strong>Barista</strong><br>
    <em>Double-win Coffee</em>
  </div>
  <div style="text-align: right;">
    Jun 2022 - Aug 2022<br>
    Shanghai, China
  </div>
</div> -->

## XTRA INFORMATION

---

- Interests: Anime, Comics & Games (ACG), cooking, gym.
