---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<div class="research-intro" id="about-me" markdown="1">
<p class="section-eyebrow">🤖 PHYSICAL AI · 🌍 WORLD MODELS · 🛡️ SAFE AI</p>

# Learning from experience. Acting in the physical world.

<div class="phd-notice" markdown="1">
**Seeking PhD opportunities** in Physical AI, world models, and safe embodied robotics. [Get in touch](mailto:Arthur12137@gmail.com) · [View CV](/Bowen_CV.pdf)
</div>

I am **Bowen Jing (荆博闻)**, Tech Lead at **Tuojing Intelligence** and a master's graduate of the **University of Manchester**. My research connects **Physical AI, World Models, and Safe AI** in embodied robotics: understanding physical interactions, anticipating action consequences, and making safety part of successful task execution.

**I approach these questions through the design of data distributions.** Within the observed distribution, policies should preserve and express meaningful behavioral preferences rather than average them away. Beyond its coverage, I pursue targeted generation of rare, safety-critical scenarios for learning and evaluation. The question is which experiences a robot needs—and how to construct and evaluate them.

My methods include **vision-language-action models (VLA)** and **world-action models (WAM)** for connecting perception, prediction, and control, alongside **diffusion and flow matching** for generative modeling and controlled sampling. These methods support learning from behavioral diversity and constructing experience beyond routine data collection.

**Reproducing a trajectory is only one part of reproducing an interaction.** My **Real2Sim / Sim2Real** agenda connects environment properties with robot dynamics, considering approach velocity, hand preshaping, contact timing and sequence, and the resulting forces, deformation, and slip. Vision and touch ground this work in physical feedback.

Long term, I want robots to pursue goals, learn from accumulated experience, and adapt through interaction, enabling safe participation in everyday human life.

<p class="profile-links"><a href="https://scholar.google.com/citations?user=7ICz8uAAAAAJ">Google Scholar ↗</a><a href="https://github.com/Bowen12137">GitHub ↗</a><a href="https://www.linkedin.com/in/bowenjing/">LinkedIn ↗</a><a href="/Bowen_CV.pdf"><strong>CV ↗</strong></a></p>
</div>

<span class="anchor" id="-publications"></span>

## Selected Research

<p class="section-lead">Three connected questions: which behavioral differences should a policy preserve, what makes an interaction acceptable, and how can we test situations that recorded experience rarely covers?</p>

<article class="selected-project" aria-labelledby="project-styledrive">
<div class="project-figure"><a href="https://styledrive.github.io/" aria-label="StyleDrive project page"><img src="_pages/images/styledrive.png" alt="StyleDrive research overview" loading="lazy"></a><span class="project-venue">AAAI 2026 · Oral</span></div>
<div class="project-body" markdown="1">
<p class="project-theme">🚗 01 / Preserve meaningful behavioral differences</p>
<h3 id="project-styledrive">StyleDrive</h3>
<p class="project-question">When several actions are valid, whose preference should a policy follow?</p>
<p class="project-role">Second author</p>

Driving demonstrations do not prescribe a single response: different drivers can make different choices in the same situation. Treating these differences as noise risks learning a default behavior that obscures individual preferences. StyleDrive makes preference an explicit part of the learning problem.

**Approach.** Style-aware annotation, preference-conditioned policies, and the SM-PDMS metric bring behavioral diversity into both learning and evaluation.

**Significance.** This extends the question from whether a policy can drive competently to whether it can do so in a way that reflects a specified preference.

<p class="project-evidence">A dataset and benchmark for personalized end-to-end driving, with an explicit measure of driving-style alignment.</p>

[**Project Page / Code**](https://styledrive.github.io/) • [**arXiv**](https://arxiv.org/abs/2506.23982) • <a class="gh-stars" href="https://github.com/AIR-THU/StyleDrive" aria-label="StyleDrive on GitHub"><img src="https://img.shields.io/github/stars/AIR-THU/StyleDrive?style=flat&amp;logo=github&amp;label=stars&amp;color=1f6feb" alt="GitHub stars for AIR-THU/StyleDrive"></a>

<details class="citation-details" markdown="1">
<summary>Paper title &amp; authors</summary>

[**StyleDrive: Towards Driving-Style Aware Benchmarking of End-To-End Autonomous Driving**](https://styledrive.github.io/)  
Ruiyang Hao, **Bowen Jing**, Haibao Yu, Zaiqing Nie  

</details>
</div>
</article>

<article class="selected-project" aria-labelledby="project-softvtbench">
<div class="project-figure"><a href="https://softvtbench.github.io/" aria-label="SoftVTBench project page"><img src="_pages/images/softvtbench.png" alt="SoftVTBench research overview" loading="lazy"></a><span class="project-venue">ECCV 2026 Workshop · Oral</span></div>
<div class="project-body" markdown="1">
<p class="project-theme">✋ 02 / Define physically acceptable success</p>
<h3 id="project-softvtbench">SoftVTBench</h3>
<p class="project-question">Is a task successful if the object is damaged along the way?</p>
<p class="project-role">First author</p>

For deformable objects, reaching the goal does not establish that the interaction was acceptable. A robot may finish the task while excessively deforming the object. SoftVTBench treats the physical consequences of contact as part of the problem definition, making this distinction measurable.

**Approach.** Synchronized visual, tactile, and action data are paired with deformation-aware tasks and FEM-based evaluation.

**Significance.** The benchmark makes physical constraints part of what a policy is evaluated against, and provides a basis for studying when touch helps distinguish task completion from acceptable interaction.

<p class="project-evidence">4,000 demonstrations · 40 tasks · 50+ deformable assets. FEM-based metrics evaluate deformation alongside task success.</p>

[**Project Page**](https://softvtbench.github.io/) • [**Tuojing Page**](https://tuojingai.github.io/?p=softvtbench) • [**arXiv**](https://arxiv.org/abs/2607.04234) • <a class="gh-stars" href="https://github.com/TuojingAI/SoftVTBench" aria-label="SoftVTBench on GitHub"><img src="https://img.shields.io/github/stars/TuojingAI/SoftVTBench?style=flat&amp;logo=github&amp;label=stars&amp;color=1f6feb" alt="GitHub stars for TuojingAI/SoftVTBench"></a>

<details class="citation-details" markdown="1">
<summary>Paper title &amp; authors</summary>

[**SoftVTBench: A Deformation-Aware Visuo-Tactile Dataset and Benchmark for Deformable-Object Manipulation**](https://arxiv.org/abs/2607.04234)  
**Bowen Jing\***, Mingxin Wang\*, Ruiyang Hao, Chenchen Ge, Hanwen Shen, Junjie He, Yang Cui, Yiming Hou, Weitao Zhou, Jiawei Wang, Minglei Li, Dandan Zhang, Ding Zhao, Houde Liu, Xiaofan Li, Si Liu, Ping Luo, Haibao Yu  

</details>
</div>
</article>

<article class="selected-project" aria-labelledby="project-counterscene">
<div class="project-figure"><a href="https://tuojingai.github.io/?p=counterscene" aria-label="CounterScene project page"><img src="_pages/images/counterscene.jpg" alt="CounterScene research overview" loading="lazy"></a><span class="project-venue">ECCV 2026 Workshop · Oral</span></div>
<div class="project-body" markdown="1">
<p class="project-theme">🌍 03 / Probe the limits of recorded experience</p>
<h3 id="project-counterscene">CounterScene</h3>
<p class="project-question">How can we expose failures that routine experience rarely reveals?</p>
<p class="project-role">First author</p>

A policy can perform well on recorded driving data while remaining vulnerable to rare interactions that those logs barely cover. CounterScene turns scenario generation into a targeted search for plausible conditions that expose these vulnerabilities.

**Approach.** Counterfactual causal reasoning and guidance during generation shape multi-agent behavior toward safety-critical interactions, which are evaluated in closed loop.

**Significance.** This gives the world model a role beyond reproducing typical behavior: it becomes a tool for actively examining the limits of a policy’s experience.

<p class="project-evidence">Closed-loop evaluation tests collision-inducing scenarios and transfer from Waymo Open Motion to nuPlan.</p>

[**Project Page**](https://tuojingai.github.io/?p=counterscene) • [**arXiv**](https://arxiv.org/abs/2603.21104) • <a class="gh-stars" href="https://github.com/TuojingAI/CounterScene" aria-label="CounterScene on GitHub"><img src="https://img.shields.io/github/stars/TuojingAI/CounterScene?style=flat&amp;logo=github&amp;label=stars&amp;color=1f6feb" alt="GitHub stars for TuojingAI/CounterScene"></a>

<details class="citation-details" markdown="1">
<summary>Paper title &amp; authors</summary>

[**CounterScene: Counterfactual Causal Reasoning in Generative World Models for Safety-Critical Closed-Loop Evaluation**](https://arxiv.org/abs/2603.21104)  
**Bowen Jing**, Ruiyang Hao, Weitao Zhou, Haibao Yu  

</details>
</div>
</article>

<span class="anchor" id="-news"></span>

## News
- *2026.09*: &nbsp;🏆 Early versions of **SoftVTBench** and **CounterScene** were accepted as **Orals** at the **Safe World Models for Trustworthy Embodied AI** workshop, [ECCV 2026](https://trustworthy-world-models.github.io/ECCV2026/).  
- *2026.08*: &nbsp;🪨 Our paper **"KnockGS: Interaction-Grounded Calibration of Physical Gaussian Representations"** is now on **arXiv**! [Read here](https://arxiv.org/abs/2608.27365) · [Code](https://github.com/TuojingAI/KnockGS)  
- *2026.07*: &nbsp;🤖 Our paper **"ST-WAM: Semantic-Temporal World Action Model for Robust Manipulation under Visual Distribution Shifts"** is now on **arXiv**! [Read here](https://arxiv.org/abs/2607.28993)  
- *2026.07*: &nbsp;🧈 Released **SoftVTBench**, a deformation-aware visuo-tactile dataset and benchmark for deformable-object manipulation. [arXiv](https://arxiv.org/abs/2607.04234) · [Project Page](https://softvtbench.github.io/)  
- *2026.03*: &nbsp;🌍 Our paper **"CounterScene: Counterfactual Causal Reasoning in Generative World Models for Safety-Critical Closed-Loop Evaluation"** is now on **arXiv**! [Read here](https://arxiv.org/abs/2603.21104)  
- *2026.03*: &nbsp;🏗️ Our paper **"ReconDrive: Fast Feed-Forward 4D Gaussian Splatting for Autonomous Driving Scene Reconstruction"** is now on **arXiv**! [Read here](https://arxiv.org/abs/2603.07552)  
- *2025.11*: &nbsp;🏆 Our work **StyleDrive** has been **accepted as an Oral presentation at AAAI 2026**.

## Additional Research

<div class="additional-project" markdown="1">

🧪 [**KnockGS: Interaction-Grounded Calibration of Physical Gaussian Representations**](https://arxiv.org/abs/2608.27365)  
Chenchen Ge\*, Hanwen Shen\*, **Bowen Jing**, Jiyuan Cai, Xiaofeng Wang, Hongsen Lei, Weitao Zhou, Dandan Zhang, Haibao Yu  

Calibrating elasticity and density from an object’s response to an applied force, then testing the estimated properties on held-out interactions.

[**Project Page**](https://tuojingai.github.io/?p=knockgs) • [**arXiv**](https://arxiv.org/abs/2608.27365) • [**Code**](https://github.com/TuojingAI/KnockGS) • <a class="gh-stars" href="https://github.com/TuojingAI/KnockGS" aria-label="KnockGS on GitHub"><img src="https://img.shields.io/github/stars/TuojingAI/KnockGS?style=flat&amp;logo=github&amp;label=stars&amp;color=1f6feb" alt="GitHub stars for TuojingAI/KnockGS"></a>

</div>

<div class="additional-project" markdown="1">

🤖 [**ST-WAM: Semantic-Temporal World Action Model for Robust Manipulation under Visual Distribution Shifts**](https://arxiv.org/abs/2607.28993)  
Mingxin Wang, Bin Hu, Bin Qian, Kaitao Jiang, Haoning Wu, Feng Yan, **Bowen Jing**, Ruiyang Hao, Enyi Wang, Kangning Niu, Yandan Yang, Mu Xu, Yan Wang, Houde Liu, Tianlun Li  

World-action modeling for manipulation under visual distribution shifts. Reported zero-shot LIBERO-Plus improvement of **21.3 points** over Fast-WAM, with real-world success under visual shift increasing from **25.8% to 61.5%**.

[**arXiv**](https://arxiv.org/abs/2607.28993) • <a class="gh-stars" href="https://github.com/Thu-WangMX/st-wam" aria-label="st-wam on GitHub"><img src="https://img.shields.io/github/stars/Thu-WangMX/st-wam?style=flat&amp;logo=github&amp;label=stars&amp;color=1f6feb" alt="GitHub stars for Thu-WangMX/st-wam"></a>

</div>

<div class="additional-project" markdown="1">

🚗 [**ReconDrive: Fast Feed-Forward 4D Gaussian Splatting for Autonomous Driving Scene Reconstruction**](https://arxiv.org/abs/2603.07552)  
Haibao Yu, Kuntao Xiao, Jiahang Wang, Ruiyang Hao, Yuxin Huang, Guoran Hu, Haifang Qin, **Bowen Jing**, Yuntian Bo, Ping Luo  

Feed-forward 4D Gaussian scene reconstruction for autonomous driving, combining static and dynamic representations for efficient novel-view synthesis.

[**Project Page**](https://tuojingai.github.io/?p=recondrive) • [**arXiv**](https://arxiv.org/abs/2603.07552) • <a class="gh-stars" href="https://github.com/TuojingAI/ReconDrive" aria-label="ReconDrive on GitHub"><img src="https://img.shields.io/github/stars/TuojingAI/ReconDrive?style=flat&amp;logo=github&amp;label=stars&amp;color=1f6feb" alt="GitHub stars for TuojingAI/ReconDrive"></a>

</div>

<div class="additional-project" markdown="1">

🚗 [**Multi-modal Sensor Fusion for End-to-End Autonomous Driving**](https://drive.google.com/file/d/1th9M1kdggCL_x-zmeAltJgVP9Lmgc4fn/view?usp=sharing)  
**Bowen Jing** — University of Manchester, MSc dissertation

My MSc dissertation investigated camera–LiDAR fusion with channel attention and GRU waypoint prediction, evaluated closed-loop in CARLA across urban scenes and weather conditions.

[**Dissertation**](https://drive.google.com/file/d/1th9M1kdggCL_x-zmeAltJgVP9Lmgc4fn/view?usp=sharing)

</div>

<span class="anchor" id="-experience"></span>

## Experience
- *2025.08 – Present* · <strong class="org org-tuojing">Tuojing Intelligence</strong> — **Tech Lead**, Real2Sim2Real and tactile simulation  
- *2025.02 – 2025.08* · <strong class="org org-tsinghua">Tsinghua University, AIR</strong> — Research Intern in **Large-Scale Autonomous Driving Data Mining**

<span class="anchor" id="-educations"></span>

## Education
- *2023.09 – 2024.09*, MSc in Advanced Computer Science, <strong class="org org-manchester">University of Manchester</strong>  
  - Focus: Deep Learning, Computer Vision, Reinforcement Learning, Robotics  
  - Dissertation: Multi-modal Sensor Fusion for End-to-End Autonomous Driving
  - Graduated with Distinction (Top 10%)

- *2020.09 – 2023.06*, BSc in Computer Science, <strong class="org org-manchester">University of Manchester</strong>  
  - Specialized in software development and machine learning foundations  
  - Final Year Project: Spiking Neural Network
