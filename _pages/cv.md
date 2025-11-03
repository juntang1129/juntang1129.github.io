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
- Service/activities: Supported classmates at Duke as Kunshan Student Orientation Peer. Led weekly training sessions as Kendo Club Training Leader...

<!-- ## HONORS & AWARDS

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
<div style="margin-top: -0.7em;"></div>
- Parsed CSV-format sequence and label data, generated YAML-format inputs, and handled data preprocessing including sequence redundancy and multi-conformation reference structures.
- Integrated and deployed a dual-model prediction pipeline (Boltz-1 & Protenix); configured cache and advanced diffusion parameters for optimal inference.
- Calculated TM-score using US-align, fused model outputs, corrected invalid coordinates, and generated compliant final submissions, achieving a top-8% finish among 1500+ teams. -->

## PROJECTS

---

**[qqgjyx.com/mheatmap](https://qqgjyx.com/mheatmap)**
[![GitHub stars](https://img.shields.io/github/stars/qqgjyx/mheatmap)](https://github.com/qqgjyx/mheatmap/stargazers)
<div style="margin-top: -0.7em;"></div>
- Developed a Python package for proportional heatmap visualization and spectral reordering that has been well received by the community (600+ GitHub stars).
- Achieved broad academic impact: the package has been adopted by multiple research groups for data visualization workflows and has been cited in peer-reviewed papers, highlighting its usefulness and reliability in published scientific research.

**[qqgjyx.com/pysgtsnepi](https://qqgjyx.com/pysgtsnepi)**
[![GitHub stars](https://img.shields.io/github/stars/qqgjyx/pysgtsnepi)](https://github.com/qqgjyx/pysgtsnepi/stargazers)
<div style="margin-top: -0.7em;"></div>
- Implemented the [SG-t-SNE-Π algorithm](https://t-sne-pi.cs.duke.edu/) in Python from scratch, making state-of-the-art dimensionality reduction more accessible to researchers.
- Achieved wider community adoption by delivering clean, well-documented APIs, enabling seamless integration of SG-t-SNE-Π into existing data science pipelines and fostering efficient usage by researchers and practitioners.

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
    <em>Signature Work</em>; Research Assistant. PI: <a href="https://faculty.dukekunshan.edu.cn/faculty_profiles/dongmian-zou" target="_blank">Prof. Dongmian Zou</a> & <a href="https://sites.google.com/site/shixinxupage/" target="_blank">Prof. Shixin Xu</a><br>
  </div>
  <div style="text-align: right;">
    Mar 2024 - Present<br>
    Kunshan, China
  </div>
</div>
<div style="margin-top: -0.7em;"></div>
- Conducted research on topics including 16S rRNA for bacterial culture media prediction and acute ischemic stroke reperfusion decision-making.
- Utilized techniques such as clustering, neural networks, and ordinary differential equations to solve real-world problems; developed novel models.
- Produced two peer-reviewed papers currently under review at top-tier international conferences, as well as one thesis.

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
- Studied how the Martian photoperiod affects the mammalian circadian system, as well as sleep and wake patterns in mice, and explored methods for vigilance state classification.
- Implemented a convolutional neural network that achieved over 90% accuracy in classifying vigilance states using mouse electroencephalography (EEG) and electromyography (EMG) data. Explored and compared more than 10 existing classification methods.
- Produced one peer-reviewed conference paper and one journal article currently under review at a PNAS sub-journal.

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
- Studied precursor clustering and community detection methods, applying them to hyperspectral imaging. Collected over 5 methods and more than 10 datasets.
- Utilized tools such as Python (scikit-learn), MATLAB, and Julia, as well as techniques such as k-nearest neighbor graphs, [Stochastic Graph t-SNE](https://t-sne-pi.cs.duke.edu/), and [Parallel Clustering with Resolution Variation](https://ieeexplore.ieee.org/document/10363552/) to address the challenge of unsupervised segmentation in hyperspectral imaging.
- Developed Python packages [mheatmap](https://qqgjyx.com/mheatmap) and [pysgtsnepi](https://qqgjyx.com/pysgtsnepi), which aid in post- and pre-processing of HSI data and have been well received by the community (600+ GitHub stars).

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
- Researched temperature-induced electronic, magnetic, and structural properties of emerging solid-state materials, including Pb$$_{10-x}$$Cu$$_x$$(PO$$_4$$)$$_6$$O$$_3$$ (LK-99), KBaLnB$$_2$$O$$_6$$ (Ln = Gd, Yb, Tb), and others.
- Utilized techniques such as temperature-dependent X-ray diffraction, Raman spectroscopy, and density functional theory (DFT) calculations to study photoluminescence, phase transitions, and ferromagnetism in these emerging or rare-earth materials.
- Produced a conference paper presented at an international conference organized by the Royal Society of Chemistry (RSC).

<!-- ## SKILLS

---

**Programming & Analysis:** Python (Advanced), MATLAB, R, Julia, Wolfram, Java, C/C++, C#, Bash  
**Data & Web:** PostgreSQL, MongoDB, HTML/CSS, Cloudflare  
**Tools:** LaTeX, Markdown, Unity, Generative AI tools (e.g., Cursor, Stable Diffusion)  
**Languages:** English (Fluent), Mandarin (Native), Japanese, French -->

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
- Assisted student residents with academic and personal issues; fostered an engaging community; handled 50+ incidents; served for 3 years.
- Developed a Python script to scrape Reddit images and the resident roster for automatic door decoration creation, which was used by fellow RAs.

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
- Assisted in backend development and conducted literature reviews on topics such as LLMs, agentic systems, and more.
- Authored a professional report on software-related industries in China, focusing on AI innovation.

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
- Assisted in investigating client businesses, including conducting credit analysis and market research.
- Drafted over 50 audit reports on local electronics companies and conducted in-depth industry research.

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

**Certifications:** Responsible Conduct for Duke Community Engagement (Canvas Credentials), Undergraduate Student Responsible Conduct of Research (CITI Program), etc. \
**Honors & awards:** <a href="https://www.kaggle.com/competitions/stanford-rna-3d-folding" target="_blank" rel="noopener">Stanford RNA 3D Folding (Kaggle)</a> Bronze Medal (Top 8%, 1500+ teams). \
**Interests:** Anime, Comics & Games (ACG), cooking, gym. \
**Service:** Supported classmates at Duke as Orientation Peer. Led weekly training sessions as Kendo Club Training Leader… \
**Skills:** Programming & analysis (Python, MATLAB, Julia, Java, C); data & web (PostgreSQL, MongoDB, HTML/CSS)…
