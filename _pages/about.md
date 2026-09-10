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

<span class='anchor' id='about-me'></span>

## About

**Bowen Jing (荆博闻)** works on **Physical AI**: robots that act in the physical world, feel through touch what their own contact is doing, and interact safely enough to be trusted around people.

<a href='https://scholar.google.com/citations?user=7ICz8uAAAAAJ'><img alt="Google Scholar citation count" src="https://img.shields.io/endpoint?url={{ url | url_encode }}&labelColor=f6f6f6&color=9cf&style=flat&label=citations&cacheSeconds=3600"></a>

> I want robots that work the way a person does with an unfamiliar task — hold a goal, use what experience has already taught them, adjust when the environment is not what they expected, and stay safe enough to belong in ordinary human spaces.

**An embodied policy is shaped by both its architecture and the data distribution it learns from.** I study two challenges: *within* the observed distribution, models can average over distinct preferences; *beyond* its coverage, rare but safety-critical situations may be missing from routine data collection.

- **Physical AI**: contact-rich manipulation and visuo-tactile perception — what touch reports about deformation, force and slip belongs in the problem, not in a sensor spec.
- **World Models**: tying observations and actions to their consequences, so experience can be generated rather than waited for — vision-language-action and world-action models, diffusion and flow matching.
- **Safe AI**: constructing safety-critical cases that are underrepresented in recorded data, and measuring harm rather than task completion.

This began with end-to-end autonomous driving during my master's. **StyleDrive** takes on the first failure, making driving preference explicit so a policy can represent distinct driving styles rather than average over them. **CounterScene** takes on the second, steering a generative world model toward safety-critical counterfactuals produced on purpose rather than met by luck. **SoftVTBench** asks what to measure once the robot is in contact: a policy can finish its task and still have crushed the object, and task success cannot see that.

I approach the simulation–reality gap from both the environment (Real2Sim) and the robot embodiment (Sim2Real), down to approach velocity and direction, hand preshaping and timing, contact location and sequence, and the forces, deformation and slip that follow. **Reproducing a trajectory is only one part of reproducing an interaction.**

Currently seeking a **PhD** in physical AI, world models, and safe embodied learning.

[Google Scholar](https://scholar.google.com/citations?user=7ICz8uAAAAAJ) • [GitHub](https://github.com/Bowen12137) • [LinkedIn](https://www.linkedin.com/in/bowenjing/) • [**CV**](/Bowen_CV.pdf)



# 🔥 News
- *2026.09*: &nbsp;🏆 Early versions of **SoftVTBench** and **CounterScene** were accepted as **Orals** at the **Safe World Models for Trustworthy Embodied AI** workshop, [ECCV 2026](https://trustworthy-world-models.github.io/ECCV2026/).  
- *2026.08*: &nbsp;🪨 Our paper **"KnockGS: Interaction-Grounded Calibration of Physical Gaussian Representations"** is now on **arXiv**! [Read here](https://arxiv.org/abs/2608.27365) · [Code](https://github.com/TuojingAI/KnockGS)  
- *2026.07*: &nbsp;🤖 Our paper **"ST-WAM: Semantic-Temporal World Action Model for Robust Manipulation under Visual Distribution Shifts"** is now on **arXiv**! [Read here](https://arxiv.org/abs/2607.28993)  
- *2026.07*: &nbsp;🧈 Released **SoftVTBench**, a deformation-aware visuo-tactile dataset and benchmark for deformable-object manipulation. [arXiv](https://arxiv.org/abs/2607.04234) · [Project Page](https://softvtbench.github.io/)  
- *2026.03*: &nbsp;🌍 Our paper **"CounterScene: Counterfactual Causal Reasoning in Generative World Models for Safety-Critical Closed-Loop Evaluation"** is now on **arXiv**! [Read here](https://arxiv.org/abs/2603.21104)  
- *2026.03*: &nbsp;🏗️ Our paper **"ReconDrive: Fast Feed-Forward 4D Gaussian Splatting for Autonomous Driving Scene Reconstruction"** is now on **arXiv**! [Read here](https://arxiv.org/abs/2603.07552)  
- *2025.11*: &nbsp;🏆 Our work **StyleDrive** has been **accepted as an Oral presentation at AAAI 2026**.  



# 📝 Publications 

<sub>\* Equal contribution. Ordered by my role in the work rather than by date.</sub>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge badge--gold-sheen">ECCV 2026 Workshop Oral</div><img src='_pages/images/counterscene.jpg' alt="counterscene" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**CounterScene: Counterfactual Causal Reasoning in Generative World Models for Safety-Critical Closed-Loop Evaluation**](https://arxiv.org/abs/2603.21104)  
**Bowen Jing**, Ruiyang Hao, Weitao Zhou, Haibao Yu  

[**Project Page**](https://tuojingai.github.io/?p=counterscene) • [**arXiv**](https://arxiv.org/abs/2603.21104) • [**ECCV 2026 Workshop (Oral)**](https://trustworthy-world-models.github.io/ECCV2026/)  
- An early version was accepted as an **Oral** at the **Safe World Models for Trustworthy Embodied AI** workshop, ECCV 2026.
- Introduced a safety-critical generative world model with **counterfactual causal reasoning** for closed-loop autonomous driving evaluation.  
- Built a **Causal Interaction Graph (CIG)** to identify conflict-aware agent relationships and guide adversarial agent selection.  
- Designed a **dynamic counterfactual guidance** strategy to optimize challenging yet realistic multi-agent trajectories during denoising.  
- Demonstrated stronger collision-inducing capability and robust transfer from **Waymo Open Motion** to **nuPlan**.  

</div></div>



<div class='paper-box'><div class='paper-box-image'><div><div class="badge badge--gold-sheen">ECCV 2026 Workshop Oral</div><img src='_pages/images/softvtbench.png' alt="softvtbench" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**SoftVTBench: A Deformation-Aware Visuo-Tactile Dataset and Benchmark for Deformable-Object Manipulation**](https://arxiv.org/abs/2607.04234)  
**Bowen Jing\***, Mingxin Wang\*, Ruiyang Hao, Chenchen Ge, Hanwen Shen, Junjie He, Yang Cui, Yiming Hou, Weitao Zhou, Jiawei Wang, Minglei Li, Dandan Zhang, Ding Zhao, Houde Liu, Xiaofan Li, Si Liu, Ping Luo, Haibao Yu  

[**Project Page**](https://softvtbench.github.io/) • [**Tuojing Page**](https://tuojingai.github.io/?p=softvtbench) • [**arXiv**](https://arxiv.org/abs/2607.04234) • [**ECCV 2026 Workshop (Oral)**](https://trustworthy-world-models.github.io/ECCV2026/)  
- An early version was accepted as an **Oral** at the **Safe World Models for Trustworthy Embodied AI** workshop, ECCV 2026.
- Released a **deformation-aware visuo-tactile benchmark** for physically constrained manipulation of deformable objects.
- Collected **4,000 expert demonstrations** across **40 tasks in 4 suites** over **50+ deformable assets**.
- Synchronized **20 Hz multimodal streams**: multi-view RGB, tactile RGB, marker motion, proprioception, language, and actions.
- Introduced **FEM-based deformation metrics** so evaluation measures what contact actually did to the object, not just task success.

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



<div class='paper-box'><div class='paper-box-image'><div><div class="badge">arXiv 2026</div><img src='_pages/images/knockgs.png' alt="knockgs" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**KnockGS: Interaction-Grounded Calibration of Physical Gaussian Representations**](https://arxiv.org/abs/2608.27365)  
Chenchen Ge\*, Hanwen Shen\*, **Bowen Jing**, Jiyuan Cai, Xiaofeng Wang, Hongsen Lei, Weitao Zhou, Dandan Zhang, Haibao Yu  

[**Project Page**](https://tuojingai.github.io/?p=knockgs) • [**arXiv**](https://arxiv.org/abs/2608.27365) • [**Code**](https://github.com/TuojingAI/KnockGS)  
- Estimated the **elasticity and density scales** of a 3D Gaussian object from its dynamics under a known applied force, instead of assuming material parameters are given.
- Turned the **force-induced response into a calibration signal**: temporal response features are extracted from the observed dynamics and the two material scales are read off them.
- **Froze the estimate and wrote it back** into the same simulator, so it is tested on an interaction it was never fitted to.
- Recovered the scales more accurately than regression, global regression, or a fixed default, measured on 3D particle trajectories, response-curve statistics, and rendered-frame quality.

</div></div>



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



<div class='paper-box'><div class='paper-box-image'><div><div class="badge">arXiv 2026</div><img src='_pages/images/recondrive.png' alt="recondrive" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**ReconDrive: Fast Feed-Forward 4D Gaussian Splatting for Autonomous Driving Scene Reconstruction**](https://arxiv.org/abs/2603.07552)  
Haibao Yu, Kuntao Xiao, Jiahang Wang, Ruiyang Hao, Yuxin Huang, Guoran Hu, Haifang Qin, **Bowen Jing**, Yuntian Bo, Ping Luo  

[**Project Page**](https://tuojingai.github.io/?p=recondrive) • [**arXiv**](https://arxiv.org/abs/2603.07552)  
- Proposed a **feed-forward 4D Gaussian scene reconstruction** framework for autonomous driving with fast novel-view synthesis.  
- Combined **DINO**, **SAM2**, and dual prediction heads to jointly estimate Gaussian parameters and centers from multi-view sequences.  
- Introduced a **static-dynamic 4D composition** design for temporally consistent scene modeling without per-scene optimization.  
- Achieved competitive reconstruction quality with substantially higher efficiency on **nuScenes** compared with optimization-based methods.  

</div></div>



<div class='paper-box'><div class='paper-box-image'><div><div class="badge">MSc Dissertation 2024</div><img src='_pages/images/e2e.png' alt="e2e" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**Multi-modal Sensor Fusion for End-to-End Autonomous Driving**](https://drive.google.com/file/d/1th9M1kdggCL_x-zmeAltJgVP9Lmgc4fn/view?usp=sharing)  
**Bowen Jing** — University of Manchester, MSc dissertation

[**Dissertation**](https://drive.google.com/file/d/1th9M1kdggCL_x-zmeAltJgVP9Lmgc4fn/view?usp=sharing)  
- Fused **camera and LiDAR in latent space** rather than at the raw or the decision level: modality-specific encoders produce feature maps that are spatially aligned and concatenated, then reweighted by **channel attention** so the planner can lean on whichever modality still carries signal — which is the whole point under the adverse weather this work targets.
- Rolled the fused latent state forward with a **GRU waypoint predictor**, so the trajectory comes out of temporal prediction over fused features instead of a single-frame regression — the same instinct that later drew me to world models.
- Evaluated **closed-loop in CARLA** across urban scenarios and weather conditions, on Driving Score, Route Completion and Infraction Score rather than open-loop imitation error.
- Placed the model deliberately on the efficiency side of the accuracy–compute trade-off: **far cheaper to run** than Transfuser- and Interfuser-class systems, at a lower absolute driving score, and argued for that point on the curve.

</div></div>



<span class="anchor" id="-educations"></span>

# 📖 Education
- *2023.09 – 2024.09*, MSc in Advanced Computer Science, University of Manchester  
  - Focus: Deep Learning, Computer Vision, Reinforcement Learning, Robotics  
  - Dissertation: Multi-modal Sensor Fusion for End-to-End Autonomous Driving
  - Graduated with Distinction (Top 10%)

- *2020.09 – 2023.06*, BSc in Computer Science, University of Manchester  
  - Specialized in software development and machine learning foundations  
  - Final Year Project: Spiking Neural Network

# 💻 Experience
- *2025.08 – Present* · **Tuojing Intelligence** — **Tech Lead**, Real2Sim2Real and tactile simulation  
- *2025.02 – 2025.08* · **Tsinghua University, AIR** — Research Intern in **Large-Scale Autonomous Driving Data Mining**
