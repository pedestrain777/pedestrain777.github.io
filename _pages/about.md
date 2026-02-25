---
permalink: /
title: "Home"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<div style="margin-bottom: 1rem;">
  <button id="lang-en-btn" onclick="switchLang('en')" style="padding: 0.45rem 0.8rem; margin-right: 0.5rem; border: 1px solid #ccc; border-radius: 6px; background: #f5f5f5; cursor: pointer;">English</button>
  <button id="lang-zh-btn" onclick="switchLang('zh')" style="padding: 0.45rem 0.8rem; border: 1px solid #ccc; border-radius: 6px; background: #fff; cursor: pointer;">中文</button>
</div>

<script>
  function switchLang(lang) {
    var en = document.getElementById('content-en');
    var zh = document.getElementById('content-zh');
    var enBtn = document.getElementById('lang-en-btn');
    var zhBtn = document.getElementById('lang-zh-btn');

    if (lang === 'zh') {
      en.style.display = 'none';
      zh.style.display = 'block';
      enBtn.style.background = '#fff';
      zhBtn.style.background = '#f5f5f5';
      localStorage.setItem('site_lang_pref', 'zh');
    } else {
      en.style.display = 'block';
      zh.style.display = 'none';
      enBtn.style.background = '#f5f5f5';
      zhBtn.style.background = '#fff';
      localStorage.setItem('site_lang_pref', 'en');
    }
  }

  document.addEventListener('DOMContentLoaded', function () {
    var saved = localStorage.getItem('site_lang_pref') || 'en'; // default English
    switchLang(saved);
  });
</script>

<div id="content-en">

## Biography

**Hengyi Zhang** is an undergraduate student in **Intelligent Science and Technology** at **Beijing University of Posts and Telecommunications (BUPT)** (Class of 2023).

Current interests focus on **efficient generative AI systems**, especially acceleration and deployment of **Diffusion / DiT-based video generation** under **cloud-edge collaborative settings**. Additional interests include model adaptation and system optimization on heterogeneous edge devices (e.g., PEFT-related deployment and evaluation).

This homepage is under active construction and will be gradually expanded with project details, publications/submissions, and technical notes.

---

## Research Interests

- Efficient Generative Models
- Video Generation Acceleration (Diffusion / DiT)
- Cloud-Edge Collaborative Inference and Scheduling
- Edge-side Deployment and System Optimization
- Parameter-Efficient Fine-Tuning (PEFT) in Practice

---

## Education

- **Beijing University of Posts and Telecommunications (BUPT)**
  - B.Eng. in Intelligent Science and Technology (Undergraduate)
  - **2023.09 – Present**
  - GPA: **3.82 / 4.00** (Average score: 91.7/100)
  - Rank: **7 / 100**
  - CET-6: **510**

---

## Research Experience Overview

### 1) School of Computer Science, Peking University (Research Internship)

Participated in research and engineering implementation on **cloud-edge collaborative acceleration for DiT-based video generation**, centered on the **EcoVideo** paradigm (currently **under review**).

**EcoVideo (under review):**
- Targets the severe latency bottleneck of the standard *step-by-step full-frame denoising* paradigm in Diffusion Transformers (DiTs) for video generation.
- Proposes an **entropy-orchestrated video generation paradigm** for dynamic cloud-edge environments.
- Uses **attention entropy** to identify informative **key frames**, reducing redundant cloud computation on low-information frames.
- Introduces a **heap-sort-based greedy interpolation algorithm** to adaptively refine complex motion regions and preserve temporal fidelity under varying frame budgets.
- Designs a **coordinated cloud-edge optimization mechanism** to map generation workloads to real-time bandwidth and edge compute availability, enabling overlap between computation and communication.
- Aims to mitigate motion breakage and detail loss while improving end-to-end throughput in dynamic distributed settings.

**Problem motivation (high-level):**
- Existing static step-splitting cloud-edge strategies often ignore inter-frame redundancy.
- Quality stability is sensitive when switching denoising responsibilities across steps/models.
- System-level latency depends strongly on dynamic bandwidth and heterogeneous compute, which is often under-evaluated in prior work.

> More public details (if available) will be added after the review stage or according to project disclosure policy.

### 2) School of Artificial Intelligence, BUPT (Research)

Participated in research on **few-step generation for discrete diffusion models**, including experiment design and validation, with a focus on balancing generation quality and efficiency.

### 3) School of Computer Science, BUPT (Research)

Participated in system-oriented research on **collaborative PEFT for large models on edge devices**, with responsibilities including deployment and testing across different edge devices and model configurations.

---

## Honors and Awards

- **Enterprise Scholarship** (award rate: **0.17%**)
- **University-Level Scholarship**
- **Outstanding Student Cadre in Mental Health Education Work (Annual)**
- **"Merit Student" Title (Two Consecutive Years)**
- **Robot Task Challenge Competition** (Team Leader): Provincial First Prize, National Second Prize  
  *(Responsible for SLAM / navigation-related module)*
- **National College Mathematics Competition**: National Second Prize

---

## Campus Experience and Personal Qualities

- Experience in student service roles (e.g., class-level psychological committee / organization-related work)
- Strong teamwork and execution ability in collaborative projects
- Long-term engagement in sports activities (e.g., football), with emphasis on discipline and consistency

---

## Contact

- **Email**: `hengyi@bupt.edu.cn`
- **GitHub**: <https://github.com/pedestrain777>

</div>

<div id="content-zh" style="display:none;">

## 个人简介

**张恒一**，北京邮电大学（BUPT）智能科学与技术专业本科生（2023级）。

当前主要关注**高效生成式人工智能系统**方向，尤其是 **Diffusion / DiT 视频生成模型**在**云边协同场景**下的加速与部署问题；同时也持续关注异构边缘设备上的模型适配与系统优化（如 PEFT 相关部署与测试）。

个人主页正在持续完善中，后续将逐步补充项目细节、论文/投稿信息以及技术笔记等内容。

---

## 研究兴趣

- 高效生成模型（Efficient Generative Models）
- 视频生成加速（Diffusion / DiT）
- 云边协同推理与调度（Cloud-Edge Collaboration）
- 边缘侧部署与系统优化
- 大模型参数高效适配（PEFT）工程实践

---

## 教育背景

- **北京邮电大学（BUPT）**
  - 智能科学与技术（本科）
  - **2023.09 – 至今**
  - GPA：**3.82 / 4.00**（均分 91.7 / 100）
  - 专业排名：**7 / 100**
  - CET-6：**510**

---

## 科研经历概览

### 1）北京大学计算机学院（科研实习）

参与 **DiT 视频生成模型云边协同加速**方向的研究与工程实现，围绕 **EcoVideo** 范式开展工作（目前仍处于**审核阶段 / under review**）。

**EcoVideo（审核中）主要内容概述：**
- 面向 Diffusion Transformers（DiTs）视频生成中“逐步、全帧去噪”带来的高时延瓶颈问题，探索动态云边协同加速方案。
- 提出面向动态云边环境的 **熵驱动（entropy-orchestrated）视频生成范式**。
- 利用 **注意力熵（Attention Entropy）** 识别信息量更高的**关键帧（key frames）**，减少云端在低信息冗余帧上的重复计算。
- 设计 **基于堆排序思想的贪心插帧算法**，对复杂运动区域进行自适应细化，以在不同预算下维持时序平滑性与细节质量。
- 结合实时带宽与边缘计算资源状态，进行云边协同负载映射与优化，实现计算与通信重叠，提升端到端吞吐效率。
- 目标是在动态云边场景中缓解运动断裂与细节损失问题，同时获得显著加速效果。

**问题动机（概括）：**
- 现有静态按步切分（step-splitting）的协同策略往往忽略视频帧间冗余；
- 在不同模型/步骤切换时，质量稳定性容易下降；
- 真实系统中的时延强烈依赖带宽波动与异构算力，系统级验证往往不足。

> 后续将在可公开范围内补充更详细的算法设计、实验设置与结果展示。

### 2）北京邮电大学人工智能学院（科研）

参与**离散扩散模型少步生成**方向研究，负责实验方案实现与验证工作，关注生成效率与视觉质量之间的平衡。

### 3）北京邮电大学计算机学院（科研）

参与边缘设备协同场景下的大模型参数高效适配（PEFT）相关系统研究，承担不同边缘设备与模型组合下的部署测试与实验支持工作。

---

## 荣誉与竞赛

- **企业奖学金**（获奖率 **0.17%**）
- **校级奖学金**
- **年度心理素质教育工作优秀学生骨干**
- **连续两届“三好学生”称号**
- **机器人任务挑战赛**（队长）：省级一等奖、国家级二等奖  
  （负责 SLAM / 导航相关模块）
- **全国大学生数学竞赛**：国家级二等奖

---

## 校园经历与个人特点

- 具有学生服务工作经历（如心理委员、组织委员等）
- 具备较强团队协作能力与执行能力
- 长期参与体育活动（如足球），重视纪律性与持续投入

---

## 联系方式

- **邮箱**：`hengyi@bupt.edu.cn`
- **GitHub**：<https://github.com/pedestrain777>

</div>
