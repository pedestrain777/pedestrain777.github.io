---
permalink: /
title: ""
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<div class="lang-root">

  <style>
    /* ---------- language toggle (small text style) ---------- */
    .lang-root {
      position: relative;
    }

    .lang-root .lang-radio {
      position: absolute;
      left: -9999px;
      opacity: 0;
      pointer-events: none;
    }

    .lang-root .lang-switch {
      display: flex;
      justify-content: flex-end;
      align-items: center;
      margin: 0.2rem 0 1.2rem 0;
      gap: 0.55rem;
      font-size: 1rem;
      line-height: 1;
    }

    .lang-root .lang-switch .sep {
      color: #888;
      margin: 0 -0.15rem;
    }

    .lang-root .lang-switch label {
      cursor: pointer;
      color: #777; /* inactive */
      text-decoration: none;
      user-select: none;
      font-weight: 500;
      border-bottom: 1px solid transparent;
      padding-bottom: 1px;
      transition: color 0.15s ease, border-color 0.15s ease;
    }

    .lang-root .lang-switch label:hover {
      color: #222; /* hover black/gray */
    }

    /* active tab: black instead of red */
    .lang-root #lang-en:checked ~ .lang-switch .label-en,
    .lang-root #lang-zh:checked ~ .lang-switch .label-zh {
      color: #111;
      border-bottom-color: #111;
      font-weight: 600;
    }

    /* language panel visibility */
    .lang-root .lang-panel {
      display: none;
    }

    .lang-root #lang-en:checked ~ .lang-panels .panel-en {
      display: block;
    }

    .lang-root #lang-zh:checked ~ .lang-panels .panel-zh {
      display: block;
    }

    /* ---------- content typography ---------- */
    .lang-root .home-sec {
      margin-top: 1.15rem;
    }

    .lang-root .home-sec h2 {
      margin: 0 0 0.55rem 0;
      font-size: 1.35rem;
      line-height: 1.25;
    }

    .lang-root .home-sec h3 {
      margin: 0.9rem 0 0.35rem 0;
      font-size: 1.02rem;
      line-height: 1.35;
    }

    .lang-root .home-sec p {
      margin: 0.35rem 0 0.55rem 0;
      line-height: 1.72;
    }

    .lang-root .home-sec ul {
      margin: 0.2rem 0 0.6rem 1.15rem;
    }

    .lang-root .home-sec li {
      margin: 0.2rem 0;
      line-height: 1.65;
    }

    .lang-root .note-block {
      border-left: 3px solid #d7d7d7;
      padding-left: 0.75rem;
      color: #666;
      margin: 0.45rem 0 0.7rem 0;
    }

    @media (max-width: 768px) {
      .lang-root .lang-switch {
        justify-content: flex-start;
        margin-top: 0.2rem;
      }
    }
  </style>

  <!-- hidden radios (default = English) -->
  <input class="lang-radio" type="radio" name="lang-toggle" id="lang-en" checked />
  <input class="lang-radio" type="radio" name="lang-toggle" id="lang-zh" />

  <!-- top-right small switch -->
  <div class="lang-switch" aria-label="Language switch">
    <label for="lang-en" class="label-en">EN</label>
    <span class="sep">/</span>
    <label for="lang-zh" class="label-zh">中文</label>
  </div>

  <div class="lang-panels">

    <!-- ===================== ENGLISH ===================== -->
    <div class="lang-panel panel-en">

      <section class="home-sec">
        <h2>Biography</h2>
        <p>
          <strong>Hengyi Zhang</strong> is an undergraduate student in
          <strong>Intelligent Science and Technology</strong> at
          <strong>Beijing University of Posts and Telecommunications (BUPT)</strong> (Class of 2023).
        </p>
        <p>
          Current interests focus on <strong>efficient generative AI systems</strong>, especially acceleration and deployment of
          <strong>Diffusion / DiT-based video generation</strong> under <strong>cloud-edge collaborative settings</strong>.
          Additional interests include model adaptation and system optimization on heterogeneous edge devices.
        </p>
        <p>
          This homepage is under active construction and will be gradually expanded with project details,
          publications/submissions, and technical notes.
        </p>
      </section>

      <section class="home-sec">
        <h2>Research Interests</h2>
        <ul>
          <li>Efficient Generative Models</li>
          <li>Video Generation Acceleration (Diffusion / DiT)</li>
          <li>Cloud-Edge Collaborative Inference and Scheduling</li>
          <li>Edge-side Deployment and System Optimization</li>
        </ul>
      </section>

      <section class="home-sec">
        <h2>Education</h2>
        <ul>
          <li><strong>Beijing University of Posts and Telecommunications (BUPT)</strong></li>
          <li>B.Eng. in Intelligent Science and Technology (Undergraduate)</li>
          <li><strong>2023.09 – Present</strong></li>
          <li>GPA: <strong>3.82 / 4.00</strong> (Average score: 91.7/100)</li>
          <li>Rank: <strong>7 / 100</strong></li>
          <li>CET-6: <strong>510</strong></li>
        </ul>
      </section>

      <section class="home-sec">
        <h2>Research Experience Overview</h2>

        <h3>1) School of Computer Science, Peking University (Research Internship)</h3>
        <p>
          Participated in research and engineering implementation on
          <strong>cloud-edge collaborative acceleration for DiT-based video generation</strong>,
          centered on the <strong>EcoVideo</strong> paradigm, <strong>submitted to ECCV 2026</strong>.
        </p>

        <p><strong>EcoVideo (submitted to ECCV 2026):</strong></p>
        <ul>
          <li>Targets the severe latency bottleneck of the standard <em>step-by-step full-frame denoising</em> paradigm in Diffusion Transformers (DiTs) for video generation.</li>
          <li>Proposes an <strong>entropy-orchestrated video generation paradigm</strong> for dynamic cloud-edge environments.</li>
          <li>Uses <strong>attention entropy</strong> to identify informative <strong>key frames</strong>, reducing redundant cloud computation on low-information frames.</li>
          <li>Introduces a <strong>heap-sort-based greedy interpolation algorithm</strong> to adaptively refine complex motion regions and preserve temporal fidelity under varying frame budgets.</li>
          <li>Designs a <strong>coordinated cloud-edge optimization mechanism</strong> to map generation workloads to real-time bandwidth and edge compute availability, enabling overlap between computation and communication.</li>
          <li>Aims to mitigate motion breakage and detail loss while improving end-to-end throughput in dynamic distributed settings.</li>
        </ul>

        <p><strong>Problem motivation (high-level):</strong></p>
        <ul>
          <li>Existing static step-splitting cloud-edge strategies often ignore inter-frame redundancy.</li>
          <li>Quality stability is sensitive when switching denoising responsibilities across steps/models.</li>
          <li>System-level latency depends strongly on dynamic bandwidth and heterogeneous compute, which is often under-evaluated in prior work.</li>
        </ul>

        <div class="note-block">
          More public details (if available) will be added according to project disclosure policy.
        </div>

        <h3>2) School of Artificial Intelligence, BUPT (Research)</h3>
        <p>
          Participated in research on <strong>few-step generation for discrete diffusion models</strong>, including experiment design and validation,
          with a focus on balancing generation quality and efficiency.
        </p>

        <h3>3) School of Computer Science, BUPT (Research)</h3>
        <p>
          Participated in system-oriented research on collaborative deployment and evaluation for large-model adaptation on edge devices,
          with responsibilities including deployment and testing across different edge devices and model configurations.
        </p>
      </section>

      <section class="home-sec">
        <h2>Honors and Awards</h2>
        <ul>
          <li><strong>Enterprise Scholarship</strong> (award rate: <strong>0.17%</strong>)</li>
          <li><strong>University-Level Scholarship</strong></li>
          <li><strong>Outstanding Student Cadre in Mental Health Education Work (Annual)</strong></li>
          <li><strong>Outstanding Student of Beijing University of Posts and Telecommunications</strong> (Two Consecutive Years)</li>
          <li><strong>Robot Task Challenge Competition</strong> (Team Leader): Provincial First Prize, National Second Prize (Responsible for SLAM / navigation-related module)</li>
          <li><strong>National College Mathematics Competition</strong>: National Second Prize</li>
        </ul>
      </section>

      <section class="home-sec">
        <h2>Campus Experience and Personal Qualities</h2>
        <ul>
          <li>Experience in student service roles (e.g., class-level psychological committee / organization-related work)</li>
          <li>Strong teamwork and execution ability in collaborative projects</li>
          <li>Long-term engagement in sports activities (e.g., football), with emphasis on discipline and consistency</li>
        </ul>
      </section>

      <section class="home-sec">
        <h2>Contact</h2>
        <ul>
          <li><strong>Email:</strong> <code>hengyi@bupt.edu.cn</code></li>
          <li><strong>GitHub:</strong> <a href="https://github.com/pedestrain777">https://github.com/pedestrain777</a></li>
        </ul>
      </section>

    </div>

    <!-- ===================== CHINESE ===================== -->
    <div class="lang-panel panel-zh">

      <section class="home-sec">
        <h2>个人简介</h2>
        <p>
          <strong>张恒一</strong>，北京邮电大学（BUPT）智能科学与技术专业本科生（2023级）。
        </p>
        <p>
          当前主要关注<strong>高效生成式人工智能系统</strong>方向，尤其是
          <strong>Diffusion / DiT 视频生成模型</strong>在<strong>云边协同场景</strong>下的加速与部署问题；
          同时也持续关注异构边缘设备上的模型适配与系统优化。
        </p>
        <p>
          个人主页正在持续完善中，后续将逐步补充项目细节、论文/投稿信息以及技术笔记等内容。
        </p>
      </section>

      <section class="home-sec">
        <h2>研究兴趣</h2>
        <ul>
          <li>高效生成模型（Efficient Generative Models）</li>
          <li>视频生成加速（Diffusion / DiT）</li>
          <li>云边协同推理与调度（Cloud-Edge Collaboration）</li>
          <li>边缘侧部署与系统优化</li>
        </ul>
      </section>

      <section class="home-sec">
        <h2>教育背景</h2>
        <ul>
          <li><strong>北京邮电大学（BUPT）</strong></li>
          <li>智能科学与技术（本科）</li>
          <li><strong>2023.09 – 至今</strong></li>
          <li>GPA：<strong>3.82 / 4.00</strong>（均分 91.7 / 100）</li>
          <li>专业排名：<strong>7 / 100</strong></li>
          <li>CET-6：<strong>510</strong></li>
        </ul>
      </section>

      <section class="home-sec">
        <h2>科研经历概览</h2>

        <h3>1）北京大学计算机学院（科研实习）</h3>
        <p>
          参与<strong>DiT 视频生成模型云边协同加速</strong>方向的研究与工程实现，围绕 <strong>EcoVideo</strong> 范式开展工作，<strong>投稿于 ECCV 2026</strong>。
        </p>

        <p><strong>EcoVideo（已投稿 ECCV 2026）主要内容概述：</strong></p>
        <ul>
          <li>面向 Diffusion Transformers（DiTs）视频生成中“逐步、全帧去噪”带来的高时延瓶颈问题，探索动态云边协同加速方案。</li>
          <li>提出面向动态云边环境的<strong>熵驱动（entropy-orchestrated）视频生成范式</strong>。</li>
          <li>利用<strong>注意力熵（Attention Entropy）</strong>识别信息量更高的<strong>关键帧（key frames）</strong>，减少云端在低信息冗余帧上的重复计算。</li>
          <li>设计<strong>基于堆排序思想的贪心插帧算法</strong>，对复杂运动区域进行自适应细化，以在不同预算下维持时序平滑性与细节质量。</li>
          <li>结合实时带宽与边缘计算资源状态，进行云边协同负载映射与优化，实现计算与通信重叠，提升端到端吞吐效率。</li>
          <li>目标是在动态云边场景中缓解运动断裂与细节损失问题，同时获得显著加速效果。</li>
        </ul>

        <p><strong>问题动机（概括）：</strong></p>
        <ul>
          <li>现有静态按步切分（step-splitting）的协同策略往往忽略视频帧间冗余；</li>
          <li>在不同模型/步骤切换时，质量稳定性容易下降；</li>
          <li>真实系统中的时延强烈依赖带宽波动与异构算力，系统级验证往往不足。</li>
        </ul>

        <div class="note-block">
          后续将在可公开范围内补充更详细的算法设计、实验设置与结果展示。
        </div>

        <h3>2）北京邮电大学人工智能学院（科研）</h3>
        <p>
          参与<strong>离散扩散模型少步生成</strong>方向研究，负责实验方案实现与验证工作，关注生成效率与视觉质量之间的平衡。
        </p>

        <h3>3）北京邮电大学计算机学院（科研）</h3>
        <p>
          参与边缘设备协同场景下的大模型适配相关系统研究，承担不同边缘设备与模型组合下的部署测试与实验支持工作。
        </p>
      </section>

      <section class="home-sec">
        <h2>荣誉与竞赛</h2>
        <ul>
          <li><strong>企业奖学金</strong>（获奖率：<strong>0.17%</strong>）</li>
          <li><strong>校级奖学金</strong></li>
          <li><strong>年度心理素质教育工作优秀学生骨干</strong></li>
          <li><strong>连续两届北京邮电大学优秀学生</strong></li>
          <li><strong>机器人任务挑战赛</strong>（队长）：省级一等奖、国家级二等奖（负责 SLAM / 导航相关模块）</li>
          <li><strong>全国大学生数学竞赛</strong>：国家级二等奖</li>
        </ul>
      </section>

      <section class="home-sec">
        <h2>校园经历与个人特点</h2>
        <ul>
          <li>具有学生服务工作经历（如心理委员、组织委员等）</li>
          <li>具备较强团队协作能力与执行能力</li>
          <li>长期参与体育活动（如足球），重视纪律性与持续投入</li>
        </ul>
      </section>

      <section class="home-sec">
        <h2>联系方式</h2>
        <ul>
          <li><strong>邮箱：</strong><code>hengyi@bupt.edu.cn</code></li>
          <li><strong>GitHub：</strong><a href="https://github.com/pedestrain777">https://github.com/pedestrain777</a></li>
        </ul>
      </section>

    </div>

  </div>
</div>
