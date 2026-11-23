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
**Seeking PhD opportunities** in Physical AI, world models, and safe embodied robotics. [Get in touch](mailto:Arthur12137@gmail.com) · [View CV](/Bowen_CV.pdf) · [中文简历](/Bowen_CV_zh.pdf)
</div>

I am **Bowen Jing (荆博闻)**, Tech Lead at **Tuojing Intelligence** and a master's graduate of the **University of Manchester**. My research connects **Physical AI, World Models, and Safe AI** in embodied robotics: understanding physical interactions, anticipating action consequences, and making safety part of successful task execution. **My core work is building physical environments for robots through Real2Sim2Real**: measuring real objects and interactions, turning them into physics-grounded simulation, and validating what is learned and evaluated there back on real robots.

**I approach these questions through the design of data distributions.** Within the observed distribution, policies should preserve and express meaningful behavioral preferences rather than average them away. Beyond its coverage, I pursue targeted generation of rare, safety-critical scenarios for learning and evaluation. The question is which experiences a robot needs—and how to construct and evaluate them.

My methods include **vision-language-action models (VLA)** and **world-action models (WAM)** for connecting perception, prediction, and control, alongside **diffusion and flow matching** for generative modeling and controlled sampling. These methods support learning from behavioral diversity and constructing experience beyond routine data collection.

**Reproducing a trajectory is only one part of reproducing an interaction.** My **Real2Sim2Real** agenda connects environment properties with robot dynamics, considering approach velocity, hand preshaping, contact timing and sequence, and the resulting forces, deformation, and slip. Vision and touch ground this work in physical feedback.

Long term, I want robots to pursue goals, learn from accumulated experience, and adapt through interaction, enabling safe participation in everyday human life.

<p class="profile-links"><a href="https://scholar.google.com/citations?user=7ICz8uAAAAAJ">Google Scholar ↗</a><a href="https://github.com/Bowen12137">GitHub ↗</a><a href="https://www.linkedin.com/in/bowenjing/">LinkedIn ↗</a><a href="/Bowen_CV.pdf"><strong>CV ↗</strong></a><a href="/Bowen_CV_zh.pdf">中文简历 ↗</a></p>
</div>

<span class="anchor" id="-publications"></span>

## Selected Research

<p class="section-lead">Four connected questions: which behavioral differences should a policy preserve, what makes an interaction acceptable, when can simulation stand in for the real robot, and how can we test situations that recorded experience rarely covers?</p>

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

[**Project Page**](https://softvtbench.github.io/) • [**Tuojing Page**](https://tuojingai.github.io/?p=softvtbench) • [**arXiv**](https://arxiv.org/abs/2608.18701) • [**Early Version (ECCVW)**](https://arxiv.org/abs/2607.04234) • <a class="gh-stars" href="https://github.com/TuojingAI/SoftVTBench" aria-label="SoftVTBench on GitHub"><img src="https://img.shields.io/github/stars/TuojingAI/SoftVTBench?style=flat&amp;logo=github&amp;label=stars&amp;color=1f6feb" alt="GitHub stars for TuojingAI/SoftVTBench"></a>

<details class="citation-details" markdown="1">
<summary>Paper title &amp; authors</summary>

[**SoftVTBench: A Deformation-Aware Visuo-Tactile Dataset and Benchmark for Deformable-Object Manipulation**](https://arxiv.org/abs/2608.18701)  
**Bowen Jing\***, Mingxin Wang\*, Ruiyang Hao, Chenchen Ge, Hanwen Shen, Junjie He, Yang Cui, Yiming Hou, Weitao Zhou, Jiawei Wang, Minglei Li, Dandan Zhang, Ding Zhao, Houde Liu, Xiaofan Li, Si Liu, Ping Luo, Haibao Yu  

</details>
</div>
</article>

<article class="selected-project" aria-labelledby="project-physfoundry">
<div class="project-figure"><img src="_pages/images/physfoundry.jpg" alt="PhysFoundry research overview" loading="lazy"><span class="project-venue">CVPR 2027 · Submission</span></div>
<div class="project-body" markdown="1">
<p class="project-theme">🦾 03 / Ground simulation in measured physics</p>
<h3 id="project-physfoundry">PhysFoundry</h3>
<p class="project-question">Can simulated dexterous tasks be trusted for both training and evaluation?</p>
<p class="project-role">First author</p>

Dexterous manipulation depends on contact, friction, and mass that are hard to guess and costly to collect on a real robot. Simulation scales data and evaluation, but only if its tasks behave like the real ones. PhysFoundry builds tasks from real measurements and checks them back on the real robot.

**Approach.** Measured shape, friction, mass and inertia, and hand–object contact are built into interactive assets; demonstration-guided generation produces simulated trajectories across four capability dimensions.

**Significance.** Six tasks set up both in simulation and on the real robot test the same frozen policies in both, so the benchmark is validated for training utility and for evaluation reliability.

<p class="project-evidence">30 tasks · 53 assets · 1,867 simulated trajectories. Trained only on PhysFoundry data, four policy families reach 20%–32% real-robot success, and simulation reproduces their ordering.</p>

<details class="citation-details" markdown="1">
<summary>Paper title &amp; authors</summary>

**PhysFoundry: A Real2Sim2Real Dataset and Benchmark for Physics-Grounded Dexterous Manipulation**  
**Bowen Jing**, et al. — CVPR 2027 submission  

</details>
</div>
</article>

<article class="selected-project" aria-labelledby="project-counterscene">
<div class="project-figure"><a href="https://tuojingai.github.io/?p=counterscene" aria-label="CounterScene project page"><img src="_pages/images/counterscene.jpg" alt="CounterScene research overview" loading="lazy"></a><span class="project-venue">CVPR 2027 Submission · ECCVW 2026 Oral</span></div>
<div class="project-body" markdown="1">
<p class="project-theme">🌍 04 / Probe the limits of recorded experience</p>
<h3 id="project-counterscene">CounterScene</h3>
<p class="project-question">How can we expose failures that routine experience rarely reveals?</p>
<p class="project-role">First author</p>

A policy can perform well on recorded driving data while remaining vulnerable to rare interactions that those logs barely cover. CounterScene turns scenario generation into a targeted search for plausible conditions that expose these vulnerabilities.

**Approach.** Every recorded encounter is kept safe by a margin: paths that stay apart, or arrivals at different times. CounterScene identifies the agent holding that margin and removes it with a progressive soft intervention on that agent alone, while the closed-loop world model generates how the ego and all other traffic respond.

**Significance.** This gives the world model a role beyond reproducing typical behavior: it becomes a tool for actively examining the limits of a policy’s experience.

<p class="project-evidence">Highest collision rate and lowest displacement error in every horizon group on nuScenes (22.7% vs. 12.3% for CCDiff over 8–10 s, at lower ADE); lowest displacement error at every horizon on nuPlan without retraining.</p>

[**Project Page**](https://tuojingai.github.io/?p=counterscene) • [**arXiv**](https://arxiv.org/abs/2603.21104) • <a class="gh-stars" href="https://github.com/TuojingAI/CounterScene" aria-label="CounterScene on GitHub"><img src="https://img.shields.io/github/stars/TuojingAI/CounterScene?style=flat&amp;logo=github&amp;label=stars&amp;color=1f6feb" alt="GitHub stars for TuojingAI/CounterScene"></a>

<details class="citation-details" markdown="1">
<summary>Paper title &amp; authors</summary>

[**CounterScene: Counterfactual Causal Reasoning in Generative World Models for Safety-Critical Closed-Loop Traffic Scenario Generation**](https://arxiv.org/abs/2603.21104)  
**Bowen Jing\***, Ruiyang Hao\*, Weitao Zhou, Haibao Yu — CVPR 2027 submission; early version at ECCV 2026 Workshop (Oral)  

</details>
</div>
</article>

<article class="selected-project" aria-labelledby="project-crashdojo">
<div class="project-figure"><a href="https://crashdojo.github.io/" aria-label="CrashDojo project page"><img src="_pages/images/crashdojo.jpg" alt="CrashDojo research overview" loading="lazy"></a><span class="project-venue">Preprint · 2026</span></div>
<div class="project-body" markdown="1">
<p class="project-theme">🚦 05 / Examine planners with accident-grounded encounters</p>
<h3 id="project-crashdojo">CrashDojo</h3>
<p class="project-question">Which actor should challenge the planner, with what maneuver, and how hard?</p>
<p class="project-role">First author</p>

A collision objective alone does not say which interaction is being tested: a lead vehicle braking and a neighbor cutting in both cause contact but demand different responses. CrashDojo turns a traffic world model into a closed-loop safety examiner whose challenges are specified before the rollout and grounded in accident evidence.

**Approach.** Road structure, participant roles, and accident evidence rank candidate actor–mechanism requests, fixing the actor, maneuver, and timing; geometry-specific guidance then steers a frozen traffic world model while adapting contact pressure to the ego response.

**Significance.** The requested interaction stays fixed while its trajectory adapts, so a planner is tested on a recognizable encounter rather than on whatever collision the generator finds.

<p class="project-evidence">Five planners on 100 nuScenes and 100 nuPlan scenes: matches or exceeds SAFE-SIM in initial-target contact in three of four groups, with fewer target–background contacts and off-road events in all four.</p>

[**Project Page**](https://crashdojo.github.io/)

<details class="citation-details" markdown="1">
<summary>Paper title &amp; authors</summary>

[**CrashDojo: Accident-Grounded World Models as Closed-Loop Safety Examiners for Autonomous Driving Planners**](https://crashdojo.github.io/)  
**Bowen Jing\***, Haoyun Tang\*, Ruiyang Hao, Chenchen Ge, Weitao Zhou, Haibao Yu  

</details>
</div>
</article>

<span class="anchor" id="-news"></span>

## News
- *2026.11*: &nbsp;🚦 **CrashDojo**: accident-grounded world models as closed-loop safety examiners for driving planners. [Project Page](https://crashdojo.github.io/)  
- *2026.11*: &nbsp;🦾 Submitted **PhysFoundry** (Real2Sim2Real benchmark for dexterous manipulation) and the full **CounterScene** paper to **CVPR 2027**.  
- *2026.10*: &nbsp;🦾 Our paper **"LLM4Robot-Bench: How Far Can GPT-6 Astra Go in Robotic Manipulation? A Hierarchical, Paired Sim-Real Benchmark"** is now on **arXiv**! [Read here](https://arxiv.org/abs/2610.34527)  
- *2026.09*: &nbsp;🏆 Early versions of **SoftVTBench** and **CounterScene** were accepted as **Orals** at the **Safe World Models for Trustworthy Embodied AI** workshop, [ECCV 2026](https://trustworthy-world-models.github.io/ECCV2026/).  
- *2026.08*: &nbsp;🪨 Our paper **"KnockGS: Interaction-Grounded Calibration of Physical Gaussian Representations"** is now on **arXiv**! [Read here](https://arxiv.org/abs/2608.27365) · [Code](https://github.com/TuojingAI/KnockGS)  
- *2026.07*: &nbsp;🤖 Our paper **"ST-WAM: Semantic-Temporal World Action Model for Robust Manipulation under Visual Distribution Shifts"** is now on **arXiv**! [Read here](https://arxiv.org/abs/2607.28993)  
- *2026.08*: &nbsp;🧈 The full **SoftVTBench** paper (4,000 demonstrations, 40 tasks, 50+ assets) is now on **arXiv**! [Read here](https://arxiv.org/abs/2608.18701)  
- *2026.07*: &nbsp;🧈 Released **SoftVTBench**, a deformation-aware visuo-tactile dataset and benchmark for deformable-object manipulation. [arXiv](https://arxiv.org/abs/2607.04234) · [Project Page](https://softvtbench.github.io/)  
- *2026.03*: &nbsp;🌍 Our paper **"CounterScene: Counterfactual Causal Reasoning in Generative World Models for Safety-Critical Closed-Loop Evaluation"** is now on **arXiv**! [Read here](https://arxiv.org/abs/2603.21104)  
- *2026.03*: &nbsp;🏗️ Our paper **"ReconDrive: Fast Feed-Forward 4D Gaussian Splatting for Autonomous Driving Scene Reconstruction"** is now on **arXiv**! [Read here](https://arxiv.org/abs/2603.07552)  
- *2025.11*: &nbsp;🏆 Our work **StyleDrive** has been **accepted as an Oral presentation at AAAI 2026**.

## Additional Research

<div class="additional-project" markdown="1">

🦾 [**LLM4Robot-Bench: How Far Can GPT-6 Astra Go in Robotic Manipulation? A Hierarchical, Paired Sim-Real Benchmark**](https://arxiv.org/abs/2610.34527)  
Haibao Yu, Jiaqi Meng, Zijian Zhang, **Bowen Jing**, Lei Yang, Yue Hu, Chenchen Ge, Yiming Hou, Chenbo Xin, Dawen Ye, Haifang Qin, Jin Li, Weitao Zhou, Jianing Qiu, Jiankai Sun, Dandan Zhang, Zaiqing Nie, Ping Luo, Ding Zhao  

Sixteen household contact-rich tasks across three cumulative levels (contact selection, force regulation, contact reconfiguration), each built in physically and visually matched simulation and real-world setups. Zero-shot real-world success falls from **80.0%** at L1 to **47.6%** at L2 and **0%** at L3; 10 of 16 tasks have identical success counts in sim and real.

[**arXiv**](https://arxiv.org/abs/2610.34527)

</div>

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
