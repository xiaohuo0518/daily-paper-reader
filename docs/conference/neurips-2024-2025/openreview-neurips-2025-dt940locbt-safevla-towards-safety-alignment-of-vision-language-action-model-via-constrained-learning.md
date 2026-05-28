---
title: "SafeVLA: Towards Safety Alignment of Vision-Language-Action Model via Constrained Learning"
title_zh: SafeVLA：通过约束学习实现视觉-语言-动作模型的安全对齐
authors: "Borong Zhang, Yuhao Zhang, Jiaming Ji, Yingshan Lei, Josef Dai, Yuanpei Chen, Yaodong Yang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=dt940loCBT"
tags: ["query:ur"]
score: 4.0
evidence: 大模型机器人安全对齐与错误分析
tldr: 视觉-语言-动作模型（VLA）在真实部署中存在安全隐患，可能导致环境、机器人或人类伤害。本文提出集成安全方法ISA，通过建模安全需求、主动诱发不安全行为、使用安全强化学习约束策略并进行评估，将安全约束显式融入VLA。该方法利用约束马尔可夫决策过程从最小最大角度优化策略。实验验证了ISA在减少不安全行为方面的有效性。该工作为机器人策略的安全部署提供了系统性方案。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-dt940locbt/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1448, \"height\": 723, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dt940locbt/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1448, \"height\": 690, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dt940locbt/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 453, \"height\": 394, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dt940locbt/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1466, \"height\": 732, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dt940locbt/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1436, \"height\": 363, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dt940locbt/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 711, \"height\": 507, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dt940locbt/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1439, \"height\": 361, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dt940locbt/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1443, \"height\": 218, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dt940locbt/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 478, \"height\": 470, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dt940locbt/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 463, \"height\": 470, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dt940locbt/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1434, \"height\": 380, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dt940locbt/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1445, \"height\": 777, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dt940locbt/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1446, \"height\": 405, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dt940locbt/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1159, \"height\": 1425, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-dt940locbt/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1451, \"height\": 526, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-dt940locbt/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1343, \"height\": 494, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dt940locbt/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 727, \"height\": 280, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dt940locbt/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1140, \"height\": 178, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dt940locbt/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1314, \"height\": 1704, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dt940locbt/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1427, \"height\": 985, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dt940locbt/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1454, \"height\": 202, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dt940locbt/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1336, \"height\": 125, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dt940locbt/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1455, \"height\": 198, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dt940locbt/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1459, \"height\": 188, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dt940locbt/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 670, \"height\": 628, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dt940locbt/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1227, \"height\": 179, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dt940locbt/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1212, \"height\": 1045, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dt940locbt/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1450, \"height\": 599, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dt940locbt/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1450, \"height\": 223, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dt940locbt/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1409, \"height\": 221, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-dt940locbt/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 763, \"height\": 529, \"label\": \"Table\"}]"
motivation: VLA模型在真实部署中存在安全隐患，需要显式集成安全约束。
method: 提出ISA框架，包括安全需求建模、不安全行为诱发、安全强化学习约束和评估。
result: 实验表明ISA能有效减少VLA策略的不安全行为，提升部署安全性。
conclusion: ISA通过约束学习为VLA模型提供了可靠的安全保证。
---

## Abstract
Vision-language-action models (VLAs) show potential as generalist robot policies. However, these models pose extreme safety challenges during real-world deployment, including the risk of harm to the environment, the robot itself, and humans. *How can safety constraints be explicitly integrated into VLAs?* We address this by exploring an integrated safety approach (ISA), systematically **modeling** safety requirements, then actively **eliciting** diverse unsafe behaviors, effectively **constraining** VLA policies via safe reinforcement learning, and rigorously **assuring** their safety through targeted evaluations. Leveraging the constrained Markov decision process (CMDP) paradigm, ISA optimizes VLAs from a min-max perspective against elicited safety risks. Thus, policies aligned through this comprehensive approach achieve the following key features: (I) effective **safety-performance trade-offs**, reducing the cumulative cost of safety violations by 83.58\% compared to the state-of-the-art method, while also maintaining task success rate (+3.85\%). (II) strong **safety assurance**, with the ability to mitigate long-tail risks and handle extreme failure scenarios. (III) robust **generalization** of learned safety behaviors to various out-of-distribution perturbations. The effectiveness is evaluated on long-horizon mobile manipulation tasks.

---

## 论文详细总结（自动生成）

# SafeVLA：通过约束学习实现视觉-语言-动作模型的安全对齐 —— 论文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：视觉-语言-动作模型（VLA）有望成为通用机器人策略，但在真实部署中面临严重的安全挑战，包括可能对环境、机器人自身和人类造成伤害。现有的LLM/VLM安全对齐方法（如RLHF、安全RLHF）无法直接适用于VLA，因为抽象的安全意图与物理世界中的具体危险之间存在巨大差异。当前VLA训练（主要依赖行为克隆或标准RL）缺乏显式集成安全约束的机制。
- **核心问题**：如何在不损失性能的前提下，将安全约束显式地集成到VLA中？
- **整体含义**：本文首次系统探索VLA安全对齐，提出集成安全方法（ISA），通过约束马尔可夫决策过程（CMDP）框架，从最小最大角度优化VLA策略，并构建了专门的安全评估基准Safety-CHORES。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：采用集成安全方法（ISA），包含四个互相关联的方面：  
  (A) **建模安全**：在CMDP框架中系统建模安全需求，定义状态-动作谓词（ϕ）和轨迹级谓词（ψ），覆盖转角、盲区、脆弱物体、关键点、危险设备等场景。  
  (B) **诱发风险**：通过大规模程序生成场景（ProcTHOR 150K + Objaverse 800K）和安全关键组件，主动诱发多样化的不安全行为，构建Safety-CHORES基准。  
  (C) **约束策略**：利用安全强化学习（SafeRL）在CMDP下进行策略优化，采用拉格朗日法将约束优化转化为无约束的min-max问题：  
    \[
    \min_{\theta} \max_{\lambda \ge 0} \left[ -J_r(\theta) + \sum_i \lambda_i J_{c_i}(\theta) \right]
    \]  
    通过交替更新策略参数θ和拉格朗日乘子λ，实现安全优先、任务性能次之的权衡。  
  (D) **安全保证**：通过测试时安全、长尾安全、极端失败安全等多维评估，确保对齐后的策略具有鲁棒性。

- **关键技术细节**：
  - 成本函数：状态-动作谓词违反时在步长t上计入成本1；轨迹级谓词违反时仅在最后一步计入成本1。
  - 成本阈值b_i设为FLaRe基线收敛成本的20%（经验选择）。
  - 训练算法基于PPO的拉格朗日变体，优化组合损失 \( L = \frac{1}{1+\lambda}(L_R - \lambda L_C) \)。
  - 策略输入为历史观测和动作序列，动作空间包含20个离散动作（移动、旋转、机械臂、抓取等）。

## 3. 实验设计：数据集/场景、基准、对比方法

- **环境与基准**：主要实验在AI2THOR模拟器上运行，使用论文自建的**Safety-CHORES**基准，包含三个长时程任务：  
  - **Safety-ObjNav**：在多个房间中导航定位目标物体。  
  - **Safety-PickUp**：在机器人前方桌面上拾取指定物体。  
  - **Safety-Fetch**：先导航找到目标物体再拾取。  
  另在iTHOR、ProcTHOR、RoboTHOR等标准基准上进行了迁移实验，以及DivScene上的零样本泛化测试。
- **对比方法**：
  - **IL+RL（标准）**：FLaRe（仅优化任务性能的RL微调）。
  - **IL+RL（奖励塑形）**：FLaRe-RS（将安全成本作为惩罚直接加入奖励）。
  - **IL-only**：SPOC（多种视觉编码器变体：DINOv2、SigLip-S/L），以及带GT检测的SPOC。
  - **RL-only**：Poliformer（仅用于导航任务）。
  - **ISA变体**：使用不同基础VLA模型（EmbCLIP、Embodied-Codebook等）验证泛化性。
- **评估指标**：任务成功率（SR）和累计成本（CC，所有安全违反的加权和）。

## 4. 资源与算力

- 论文明确指出：所有实验在 **8块NVIDIA H100 GPU** 上运行，使用PyTorch 2.0.1、CUDA 12.2，系统为Ubuntu 20.04.2 LTS。
- 训练步数：简单任务（Safety-ObjNav、Safety-PickUp）训练 **1500万步**，复杂任务（Safety-Fetch）训练 **2500万步**。
- 未提供具体训练时长（小时数），但表明使用分布式采样（8 GPU × 每设备4环境 = 32并行rollout）。

## 5. 实验数量与充分性

- **实验数量丰富**：涵盖三大任务（ObjNav、PickUp、Fetch），每个任务都有主对比实验。
- **消融实验**：
  - 风险诱发的必要性（去掉安全关键组件的简化场景）。
  - 不同成本阈值b_i（10%、20%、50%）。
  - 固定惩罚系数 vs 拉格朗日动态乘子。
  - 不同SafeRL算法（PID-Lagrangian、Augmented-Lagrangian）。
  - 不同基础VLA模型（4种×多个基准）。
- **鲁棒性实验**：4种OOD扰动（颜色、光照、材质、全部组合），极端失败场景（任务成功率接近0%），语义/感知扰动（同义词、结构变化、图像翻转等）。
- **零样本泛化**：在DivScene（81种未见场景类型）上测试。
- **泛化到未见安全谓词**：通过GPT-4识别5种新谓词，验证覆盖率>95%。
- **Sim-to-Real初步验证**：在真实机器人平台上部署Safety-PickUp任务。
- **公平性**：对比方法使用相同的IL基础模型（SPOC-DINOv2）或相同训练步数；实验结果以表格和统计检验（T检验、皮尔逊相关、逻辑回归）支撑结论。  
  总体而言，实验设计充分、客观，覆盖了主要维度，结论可靠。

## 6. 论文的主要结论与发现

- **安全-性能权衡优秀**：相比最强任务RL基线FLaRe，ISA平均降低累计成本 **83.58%**，同时任务成功率提升 **3.85%**。
- **消除高风险轨迹**：ISA将不安全行为严重程度的上界降低至FLaRe的1/35，大幅减少灾难性安全故障。
- **安全与任务解耦**：ISA的安全行为与任务成功与否弱相关（T检验拒绝相关性），而FLaRe中高成本与失败显著相关（p<0.01）。
- **鲁棒泛化**：
  - OOD扰动下安全成本仅小幅增加，任务性能保持稳定。
  - 极端失败场景中ISA累计成本仅2.20，远低于FLaRe（71.68）和SPOC（14.63）。
  - 零样本泛化到DivScene和未见安全谓词，表现优异。
- **拉格朗日动态乘子优于固定惩罚**，能更好地平衡安全与任务。
- **Safety-CHORES基准**能有效暴露VLA的安全漏洞（成本是标准基准的2倍以上）。

## 7. 优点

- **首次系统探索VLA安全对齐**：将SafeRL与CMDP框架应用于VLA，提出完整ISA流程，填补了显式安全集成的空白。
- **方法论全面**：从建模、诱发、约束到保证，形成闭环，且每个环节都有具体实现（如形式化谓词、触发成本定义等）。
- **基准创新**：构建Safety-CHORES基准，包含多种安全关键组件和长时程任务，更贴近真实危险场景。
- **实验严谨**：大量消融、OOD、极端失败、零样本泛化、Sim-to-Real验证，统计检验支撑结论。
- **开放性与可复现性**：代码、模型、数据、基准环境均开源，许可为CC BY-NC 4.0。
- **可扩展性**：支持不同类型的VLA模型和不同SafeRL算法。

## 8. 不足与局限

- **主要依赖仿真**：尽管有Sim-to-Real初步验证，但大量实验仍在模拟中进行，真实世界的动力学不匹配、传感器噪声、不可逆后果等挑战尚未充分解决。
- **成本赋值简略**：对于轨迹级谓词，仅将成本归因于最终步，可能导致信用分配不佳，未来可探索更精细的启发式方法。
- **安全约束为二值且均匀**：未区分严重程度或与语言指令关联，实际场景中不同违规的严重性高度依赖上下文。
- **标签依赖**：安全谓词的实现需要场景几何和语义信息（如物体分类、位置），在开放世界或未知环境中难以完全自动化。
- **训练成本高**：需要大量仿真交互（千万级步数）和多GPU资源，可能限制实际部署的可访问性。
- **未考虑物理约束**：方法基于强化学习，未与基于模型的控制或屏障函数等正式安全保证方法结合，无法提供数学上的零违规保证。

（完）
