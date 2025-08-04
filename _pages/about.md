---
permalink: /
title: ""
excerpt: ""
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

<span class='anchor' id='about-me'></span>

I am a Master’s graduate in Artificial Intelligence from the University of Manchester, with a deep passion for building intelligent systems that learn, perceive, and act in the real world. My research bridges **deep learning**, **generative modeling**, and **autonomous systems**, with a focus on enabling robust, interpretable, and generalizable AI agents.

My long-term goal is to develop autonomous agents capable of *accurate perception*, *goal-directed decision making*, and *continual learning* in complex, uncertain environments. In particular, I am fascinated by **diffusion models**, **vision-language systems**, and **embodied intelligence**. I believe these are key ingredients for the next generation of interactive AI systems.

I have hands-on experience in:
- End-to-end autonomous driving and personalized trajectory generation;
- Multimodal learning (vision, language, control);
- Video generation, GNNs, reinforcement learning, and real-world dataset curation.

Currently, I am seeking a PhD position in the UK or globally where I can explore the intersection of **generative models**, **robotics**, and **embodied cognition**.

> If you're building the future of grounded, generative, and human-aligned AI — let’s connect.

[Google Scholar](https://scholar.google.com/) • [GitHub](https://github.com/) • [LinkedIn](https://linkedin.com/)



# 🔥 News
- *2025.07*: &nbsp;🚀 Our paper **"StyleDrive: Towards Driving-Style Aware Benchmarking of End-to-End Autonomous Driving"** is now on arXiv! [Read here](https://arxiv.org/abs/2506.23982)
- *2025.06*: &nbsp;🎉 I received a Distinction (85%) for my Master's final project on comparative analysis of Deep Learning vs Traditional CV in robotic perception, ranking top 10% in class.


# 📝 Publications 

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Research Project 2025</div><img src='_pages/images.png' alt="styledrive" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**StyleDrive: Driving-Style Aware Benchmarking of End-to-End Autonomous Driving**](https://github.com/AIR-THU/StyleDrive)  
**Bowen Jing**, Ruiyang Hao, Haibao Yu, Zaiqing Nie  

[**Project Page / Code**](https://github.com/AIR-THU/StyleDrive)  
- Constructed the first real-world large-scale dataset for driving-style aware E2EAD, with 30k+ annotated scenarios.  
- Proposed a hybrid annotation framework combining motion heuristics and VLM-based reasoning.  
- Designed SM-PDMS metric and benchmarked multiple E2E models (e.g., DiffusionDrive, TransFuser) with style conditioning.  
</div></div>


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Research Project 2025</div><img src='_pages/images/translation.png' alt="signbart" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**SignBart: Gloss-Free Sign Language Translation for Human-Robot Interaction via Efficient Spatiotemporal Learning**]
**Bowen Jing**, Hongpeng Wang, Hao Tang, Xiang Li, Fanying Kong

[**Preprint (Submitted to ICRA 2026)**]  
- Proposed a gloss-free, end-to-end sign language translation framework tailored for human-robot interaction scenarios.  
- Designed a lightweight visual encoder **CSIFE-ConvNeXt**, leveraging channel-separated large kernel convolutions to reduce 58% parameters while preserving spatiotemporal expressiveness.  
- Introduced **TTT-mBART**, a test-time training enhanced decoder that enables dynamic domain adaptation and low-complexity semantic modeling during inference.  
- Outperformed prior gloss-free methods (GFSLT, SignBERT+) on PHOENIX-2014T and CSL-Daily datasets in BLEU-4 and ROUGE scores, with stronger long-form translation capabilities.  
- Demonstrated practical deployability for assistive and service robots under low-resource and variable-environment settings.
</div></div>



<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Course Project 2024</div><img src='_pages/images/e2e.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**End-to-End Autonomous Driving System with Middle Fusion and Attention**](https://drive.google.com/file/d/1th9M1kdggCL_x-zmeAltJgVP9Lmgc4fn/view?usp=sharing)  
**Bowen Jing**

[**Project Report**](https://drive.google.com/file/d/1th9M1kdggCL_x-zmeAltJgVP9Lmgc4fn/view?usp=sharing)  
- Built a multimodal AV system integrating LiDAR and RGB via channel-attentive fusion.
- Deployed in CARLA and validated via extensive ablation studies.
</div></div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">NeurIPS Submission 2025</div><img src='_pages/images/resolution.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**VDiff-SR: Diffusion with Hierarchical Visual Autoregressive Priors for Image Super-Resolution**](https://anonymous.4open.science/r/VDiff-SR-SR-F32022)  
**Bowen Jing**

[**Paper**](https://anonymous.4open.science/r/VDiff-SR-SR-F32022)  
- Proposed a novel hybrid framework combining diffusion models and pretrained Visual AutoRegressive (VAR) priors for real-world image super-resolution (Real-ISR).
- Designed two new modules: Condition-Gated Unit (CoGU) for feature conditioning, and Cross-Scale Prior-Aligned Attention (CSPA) for multi-scale structural alignment.
- Achieved SOTA performance on RealSR and RealSet5 with significant improvements in perceptual metrics (CLIP-IQ ↑, MUSIQ ↑).
- Conducted detailed ablation demonstrating the synergy of VAR priors and denoising-based generation.
</div></div>


# 📖 Educations
- *2023.09 – 2025.07 (Expected)*, MSc in Artificial Intelligence, University of Manchester  
  - Focus: Deep Learning, Computer Vision, Reinforcement Learning, Robotics  
  - Dissertation: Comparative study of Deep Learning and Traditional Vision in Robotic Perception  
  - Graduated with Distinction (Top 10%)

- *2019.09 – 2023.06*, BEng in Computer Science and Technology, [Your Undergraduate University Name]  
  - Specialized in software development and machine learning foundations  
  - Final Year Project: Multi-modal gesture recognition using CNNs and IMU sensors

