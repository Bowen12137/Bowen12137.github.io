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

## About

**Bowen Jing (荆博闻)** works on **Physical AI** and **Safe AI**: embodied agents that act in the physical world, and the world models and evaluation needed before we can trust them there.

<a href='https://scholar.google.com/citations?user=7ICz8uAAAAAJ'><img src="https://img.shields.io/endpoint?url={{ url | url_encode }}&labelColor=f6f6f6&color=9cf&style=flat&label=citations&cacheSeconds=3600"></a>

My question is **what an embodied agent must understand about physical dynamics before it can be trusted to act around people — and how we would know whether it does.** I build world models that capture how environments respond to contact, policies that hold up under conditions they were not trained on, and evaluation that measures harm rather than task success alone.

- **Physical AI**: contact-rich manipulation, visuo-tactile perception, deformable-object interaction
- **World Models**: environment dynamics and generative simulation faithful enough to serve as a testbed for decision-making
- **Safe AI**: counterfactual scenario generation, robustness under distribution shift, and evaluation that surfaces failure before deployment

This began in **autonomous driving**, where safety-critical evaluation is unavoidable. I now carry the same tools into **robot manipulation and household environments**, where failure is tangible and the object being handled can be damaged.

> Long term: bring robots out of the laboratory and into ordinary homes and human society — capable enough to be useful, and safe enough to be trusted.

Currently seeking a **PhD** in physical AI, world models, and AI safety for embodied systems.

[Google Scholar](https://scholar.google.com/citations?user=7ICz8uAAAAAJ) • [GitHub](https://github.com/Bowen12137) • [LinkedIn](https://www.linkedin.com/in/bowenjing/) • [**CV**](/Bowen_CV.pdf)



# 🔥 News
- *2026.09*: &nbsp;🏆 Early versions of **SoftVTBench** and **CounterScene** were accepted as **Orals** at the **Safe World Models for Trustworthy Embodied AI** workshop, [ECCV 2026](https://trustworthy-world-models.github.io/ECCV2026/).  
- *2026.07*: &nbsp;🤖 Our paper **"ST-WAM: Semantic-Temporal World Action Model for Robust Manipulation under Visual Distribution Shifts"** is now on **arXiv**! [Read here](https://arxiv.org/abs/2607.28993)  
- *2026.07*: &nbsp;🧈 Released **SoftVTBench**, a deformation-aware visuo-tactile dataset and benchmark for deformable-object manipulation. [arXiv](https://arxiv.org/abs/2607.04234) · [Project Page](https://softvtbench.github.io/)  
- *2026.03*: &nbsp;🌍 Our paper **"CounterScene: Counterfactual Causal Reasoning in Generative World Models for Safety-Critical Closed-Loop Evaluation"** is now on **arXiv**! [Read here](https://arxiv.org/abs/2603.21104)  
- *2026.03*: &nbsp;🏗️ Our paper **"ReconDrive: Fast Feed-Forward 4D Gaussian Splatting for Autonomous Driving Scene Reconstruction"** is now on **arXiv**! [Read here](https://arxiv.org/abs/2603.07552)  
- *2025.11*: &nbsp;🏆 Our work **StyleDrive** has been **accepted as an Oral presentation at AAAI 2026**.  



# 📝 Publications 

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">arXiv 2026</div><img src='_pages/images/stwam.png' alt="stwam" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**ST-WAM: Semantic-Temporal World Action Model for Robust Manipulation under Visual Distribution Shifts**](https://arxiv.org/abs/2607.28993)  
Mingxin Wang, Bin Hu, Bin Qian, Kaitao Jiang, Haoning Wu, Feng Yan, **Bowen Jing**, Ruiyang Hao, Enyi Wang, Kangning Niu, Yandan Yang, Mu Xu, Yan Wang, Houde Liu, Tianlun Li  

[**arXiv**](https://arxiv.org/abs/2607.28993)  
- Identified **Training-Distribution Hallucination**: pixel-generative future supervision hallucinates training-domain content instead of staying faithful to a visually shifted scene.
- Showed via a controlled frame-triplet diagnosis that **DINOv3 features stay more stable across visual shifts** than Wan-VAE latents while better preserving task-state distinctions.
- Proposed **Dual-Space Future Experts (DSFE)** and **Current-Anchored Intent Retrieval (CAIR)**, trained end-to-end with **no explicit future generation at inference**.
- Reached **98.7% on LIBERO** and **92.8% on RoboTwin 2.0**; improved zero-shot LIBERO-Plus by **21.3 points** over Fast-WAM and lifted real-world success under visual shift from **25.8% to 61.5%**.

</div></div>



<div class='paper-box'><div class='paper-box-image'><div><div class="badge badge--gold-sheen">ECCV 2026 Workshop Oral</div><img src='_pages/images/softvtbench.png' alt="softvtbench" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**SoftVTBench: A Deformation-Aware Visuo-Tactile Dataset and Benchmark for Deformable-Object Manipulation**](https://arxiv.org/abs/2607.04234)  
**Bowen Jing\***, Mingxin Wang\*, Ruiyang Hao, Chenchen Ge, Hanwen Shen, Junjie He, Yang Cui, Yiming Hou, Weitao Zhou, Jiawei Wang, Minglei Li, Dandan Zhang, Ding Zhao, Houde Liu, Xiaofan Li, Si Liu, Ping Luo, Haibao Yu  

[**Project Page**](https://softvtbench.github.io/) • [**arXiv**](https://arxiv.org/abs/2607.04234) • [**ECCV 2026 Workshop (Oral)**](https://trustworthy-world-models.github.io/ECCV2026/)  
- An early version was accepted as an **Oral** at the **Safe World Models for Trustworthy Embodied AI** workshop, ECCV 2026.
- Released a **deformation-aware visuo-tactile benchmark** for physically constrained manipulation of deformable objects.
- Collected **4,000 expert demonstrations** across **40 tasks in 4 suites** over **50+ deformable assets**.
- Synchronized **20 Hz multimodal streams**: multi-view RGB, tactile RGB, marker motion, proprioception, language, and actions.
- Introduced **FEM-based deformation metrics** so evaluation measures what contact actually did to the object, not just task success.

</div></div>



<div class='paper-box'><div class='paper-box-image'><div><div class="badge badge--gold-sheen">ECCV 2026 Workshop Oral</div><img src='_pages/images/counterscene.jpg' alt="counterscene" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**CounterScene: Counterfactual Causal Reasoning in Generative World Models for Safety-Critical Closed-Loop Evaluation**](https://arxiv.org/abs/2603.21104)  
**Bowen Jing**, Ruiyang Hao, Weitao Zhou, Haibao Yu  

[**arXiv**](https://arxiv.org/abs/2603.21104) • [**ECCV 2026 Workshop (Oral)**](https://trustworthy-world-models.github.io/ECCV2026/)  
- An early version was accepted as an **Oral** at the **Safe World Models for Trustworthy Embodied AI** workshop, ECCV 2026.
- Introduced a safety-critical generative world model with **counterfactual causal reasoning** for closed-loop autonomous driving evaluation.  
- Built a **Causal Interaction Graph (CIG)** to identify conflict-aware agent relationships and guide adversarial agent selection.  
- Designed a **dynamic counterfactual guidance** strategy to optimize challenging yet realistic multi-agent trajectories during denoising.  
- Demonstrated stronger collision-inducing capability and robust transfer from **Waymo Open Motion** to **nuPlan**.  

</div></div>



<div class='paper-box'><div class='paper-box-image'><div><div class="badge">arXiv 2026</div><img src='_pages/images/recondrive.png' alt="recondrive" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**ReconDrive: Fast Feed-Forward 4D Gaussian Splatting for Autonomous Driving Scene Reconstruction**](https://arxiv.org/abs/2603.07552)  
Haibao Yu, Kuntao Xiao, Jiahang Wang, Ruiyang Hao, Yuxin Huang, Guoran Hu, Haifang Qin, **Bowen Jing**, Yuntian Bo, Ping Luo  

[**arXiv**](https://arxiv.org/abs/2603.07552)  
- Proposed a **feed-forward 4D Gaussian scene reconstruction** framework for autonomous driving with fast novel-view synthesis.  
- Combined **DINO**, **SAM2**, and dual prediction heads to jointly estimate Gaussian parameters and centers from multi-view sequences.  
- Introduced a **static-dynamic 4D composition** design for temporally consistent scene modeling without per-scene optimization.  
- Achieved competitive reconstruction quality with substantially higher efficiency on **nuScenes** compared with optimization-based methods.  

</div></div>



<div class='paper-box'><div class='paper-box-image'><div><div class="badge badge--gold-sheen">AAAI 2026 Oral</div><img src='_pages/images/styledrive.png' alt="styledrive" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**StyleDrive: Towards Driving-Style Aware Benchmarking of End-To-End Autonomous Driving**](https://styledrive.github.io/)  
Ruiyang Hao, **Bowen Jing**, Haibao Yu, Zaiqing Nie  

[**Project Page / Code**](https://styledrive.github.io/) • [**arXiv**](https://arxiv.org/abs/2506.23982)  
- 🚗 Introduced the **first large-scale real-world dataset** for driving-style–aware E2E autonomous driving.  
- 🧠 Developed a **hybrid annotation pipeline** combining motion heuristics and VLM reasoning.  
- 📊 Proposed the **SM-PDMS metric** and established the **first benchmark** for personalized E2EAD.  
- 💡 Achieved **notable improvements in human-like driving** through style conditioning.  

</div></div>



<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Master Dissertation 2024</div><img src='_pages/images/e2e.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**End-to-End Autonomous Driving System with Middle Fusion and Attention**](https://drive.google.com/file/d/1th9M1kdggCL_x-zmeAltJgVP9Lmgc4fn/view?usp=sharing)  
**Bowen Jing**

[**Project Report**](https://drive.google.com/file/d/1th9M1kdggCL_x-zmeAltJgVP9Lmgc4fn/view?usp=sharing)  
- Built a multimodal AV system integrating LiDAR and RGB via channel-attentive fusion.
- Deployed in CARLA and validated via extensive ablation studies.
</div></div>



# 📖 Educations
- *2023.09 – 2024.09*, MSc in Artificial Intelligence, University of Manchester  
  - Focus: Deep Learning, Computer Vision, Reinforcement Learning, Robotics  
  - Dissertation: Comparative study of Deep Learning and Traditional Vision in Robotic Perception  
  - Graduated with Distinction (Top 10%)

- *2020.09 – 2023.06*, BSc in Computer Science, University of Manchester  
  - Specialized in software development and machine learning foundations  
  - Final Year Project: Spiking Neural Network

# 💻 Experience
- *2025.08 – Present* · **Tuojing Intelligence** — **Tech Lead**, Real2Sim2Real and tactile simulation  
- *2025.02 – 2025.08* · **Tsinghua University, AIR** — Research Intern in **Large-Scale Autonomous Driving Data Mining**
