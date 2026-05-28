---
title: "CooHOI: Learning Cooperative Human-Object Interaction with Manipulated Object Dynamics"
title_zh: CooHOI：通过学习操纵物体动力学实现协作式人机交互
authors: "Jiawei Gao, Ziqin Wang, Zeqi Xiao, Jingbo Wang, Tai Wang, Jinkun Cao, Xiaolin Hu, Si Liu, Jifeng Dai, Jiangmiao Pang"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=iYzyTmd3Jd"
tags: ["query:ur"]
score: 5.0
evidence: 多个人形机器人协作中的数据稀缺问题
tldr: 该论文提出CooHOI框架解决多人形机器人协同搬运问题。针对多智能体运动捕捉数据稀缺，采用两阶段学习范式：先学习单个智能体技能，再通过策略微调实现协作。在仿真环境中验证了有效性，其数据效率和迁移方法可为人形机器人数据集构建提供思路。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-iyzytmd3jd/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1445, \"height\": 883, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-iyzytmd3jd/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1429, \"height\": 615, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-iyzytmd3jd/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1425, \"height\": 271, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-iyzytmd3jd/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1434, \"height\": 677, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-iyzytmd3jd/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1436, \"height\": 426, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-iyzytmd3jd/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1164, \"height\": 679, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-iyzytmd3jd/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1425, \"height\": 459, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-iyzytmd3jd/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1429, \"height\": 564, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-iyzytmd3jd/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1460, \"height\": 286, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-iyzytmd3jd/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1235, \"height\": 280, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-iyzytmd3jd/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 544, \"height\": 536, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-iyzytmd3jd/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 752, \"height\": 465, \"label\": \"Table\"}]"
motivation: 多人形机器人协作缺乏运动捕捉数据，且多智能体学习效率低。
method: 两阶段学习：先单独学习每个机器人的技能，再联合训练协作策略。
result: 在物体运输任务上成功率高于基线，且数据效率高。
conclusion: CooHOI有效克服了多智能体数据稀缺问题，可推广到其他协作场景。
---

## Abstract
Enabling humanoid robots to clean rooms has long been a pursued dream within humanoid research communities. However, many tasks require multi-humanoid collaboration, such as carrying large and heavy furniture together. Given the scarcity of motion capture data on multi-humanoid collaboration and the efficiency challenges associated with multi-agent learning, these tasks cannot be straightforwardly addressed using training paradigms designed for single-agent scenarios. In this paper, we introduce **Coo**perative **H**uman-**O**bject **I**nteraction (**CooHOI**), a framework designed to tackle the challenge of multi-humanoid object transportation problem through a two-phase learning paradigm: individual skill learning and subsequent policy transfer. First, a single humanoid character learns to interact with objects through imitation learning from human motion priors. Then, the humanoid learns to collaborate with others by considering the shared dynamics of the manipulated object using centralized training and decentralized execution (CTDE) multi-agent RL algorithms. When one agent interacts with the object, resulting in specific object dynamics changes, the other agents learn to respond appropriately, thereby achieving implicit communication and coordination between teammates. Unlike previous approaches that relied on tracking-based methods for multi-humanoid HOI, CooHOI is inherently efficient, does not depend on motion capture data of multi-humanoid interactions, and can be seamlessly extended to include more participants and a wide range of object types.

---

## 论文详细总结（自动生成）

# 论文总结：CooHOI：通过学习操纵物体动力学实现协作式人机交互

## 1. 核心问题与整体含义

- **研究动机**：人形机器人进行大件家具搬运等任务需要多机器人协作，但多机器人协作的运动捕捉数据极度稀缺，且直接使用多智能体强化学习训练效率低下、难以收敛。现有方法（如跟踪式方法）依赖昂贵的多人交互数据，且难以扩展到不同物体和更多智能体。
- **整体含义**：论文旨在解决“多个人形机器人协同搬运物体”这一挑战，提出了一个无需多人交互数据、仅需单个人体运动捕捉数据即可训练协作策略的框架，实现了高效、可扩展的协作人机交互。

## 2. 方法论的核心思想与关键技术细节

- **核心思想**：两阶段学习范式（Two-Phase Learning Paradigm）——先单独学习每个智能体的物体搬运技能，再通过基于物体动力学的隐式通信机制，将技能迁移到多智能体协作场景。
- **第一阶段：单智能体技能学习**
  - 使用对抗性运动先验（AMP）框架，通过模仿学习从人类运动数据中获得自然行为。
  - 将操作物体的动力学信息（物体包围盒八个顶点、旋转角、线速度、角速度）纳入观测空间（公式1、2），使智能体感知自身动作对物体的影响。
  - 将搬运任务分解为三个子任务：走向物体、抬起物体、搬运到目标，并设计对应的奖励函数（r_walk, r_held, r_target），同时引入“站立点”（stand points）和“握持点”（held points）辅助技能迁移。
- **第二阶段：多智能体协作学习**
  - 将单智能体策略复制到每个智能体，并进行微调。通过让每个智能体观察长物体末端的局部包围盒动力学信息（相当于模拟搬运一个小盒子），实现技能平滑迁移。
  - 利用物体刚体特性实现隐式通信：一个智能体的动作改变物体动力学，其他智能体通过观察物体动力学变化自动调整行为。
  - 采用集中训练-分散执行（CTDE）模式，使用多智能体PPO（MAPPO）算法训练，并共享所有智能体的策略和值网络参数。
- **公式与算法**：奖励函数由任务奖励（加权组合）和风格奖励（来自AMP判别器）组成；MAPPO通过更新值网络（公式6）优化累积折扣奖励。

## 3. 实验设计

- **数据集与场景**：
  - 运动数据来源：AMASS数据集（ACCAD子集），收集了4类共26个参考动作（走路、捡起、搬运、放下、侧走、倒走）。
  - 测试物体：盒子（Box）以及三种日常物体（桌子、扶手椅、高脚凳）用于单人搬运，沙发（Sofa）用于双人搬运。物体尺寸、重量、搬运距离随机初始化。
  - 环境：Isaac Gym物理仿真器，60Hz仿真频率，策略控制频率30Hz。
- **基准方法**：
  - 单智能体场景：对比InterPhys（跟踪式方法）与提出的CooHOI（含/不含权重增强）。
  - 多智能体场景：对比从零开始训练的“From Scratch”方法与CooHOI。
- **评估指标**：成功率（Success Rate，物体与目标距离<0.2m）和精度（Precision，所有成功任务中物体与目标的平均距离）。

## 4. 资源与算力

- **计算资源**：单块Nvidia GTX 3090Ti GPU。
- **训练时长**：4096个并行环境，15,000个epoch，约15小时完成训练。
- **说明**：文中明确给出了GPU型号、并行环境数量、训练时长，信息完整。

## 5. 实验数量与充分性

- **实验数量**：论文报告了以下主要实验：
  - 单智能体和双智能体盒子搬运性能对比（表1）。
  - 对多种日常物体（桌子、扶手椅、高脚凳、沙发）的成功率和精度（表2）。
  - 单智能体政策鲁棒性分析：物体形状、尺寸、重量、搬运距离的影响（图5）。
  - 双智能体边界测试：对大物体、小物体的成功率分析（图5）。
  - 消融实验：移除“站立点”、“动力学观测”、“倒走能力”、“预训练初始化”等组件的影响（图8及失败案例可视化图7）。
  - 噪声鲁棒性测试：在观测中加入高斯噪声（表4）。
- **充分性与公平性**：
  - 与InterPhys等基线进行了公平对比（控制重量范围等）。
  - 消融实验覆盖了所有关键设计，并展示了失败案例，有助于理解各组件贡献。
  - 使用了4个随机种子取平均值，并报告了误差信息（图8中显示了阴影区域）。
  - 总体而言，实验设计较为全面客观。

## 6. 主要结论与发现

- CooHOI框架能有效训练人形机器人协作搬运物体，仅需单智能体运动数据，无需多人交互数据。
- 双智能体协作比单智能体能搬运更重更大的物体，但协调复杂度增加导致边界条件更敏感。
- 物体动力学作为隐式通信通道是实现高效协作的关键。
- 消融实验表明，站立点、动力学观测、倒走动作和单智能体预训练初始化都是不可或缺的。
- 该方法可扩展至多种日常物体（桌子、沙发等）和更多数量智能体（文中提到了四智能体场景的初步测试）。

## 7. 优点

- **数据高效**：仅需单个人体运动捕捉数据，无需昂贵的多人交互数据。
- **可扩展性强**：可平滑扩展到不同物体类型和不同数量的智能体（如四智能体）。
- **通信自然**：利用物体动力学变化实现隐式通信，避免了显式通信的复杂性。
- **框架通用性**：两阶段学习范式可推广到其他多机器人协作任务。
- **实验充分**：进行了全面的消融、边界测试和噪声鲁棒性分析，验证了每个设计选择的重要性。

## 8. 不足与局限

- **缺乏灵巧手**：智能体没有灵巧的手指，无法操纵光滑或易滑落的物体，也无法进行精细操作。
- **形状泛化有限**：使用简单的包围盒作为物体表示，限制了框架对不同物体形状的泛化能力，需要为每种物体类型单独训练。
- **未见真实部署**：所有实验仅在仿真环境中进行，未在真实人形机器人上验证。
- **重量泛化受限**：策略未输入物体密度/重量信息，导致对不同重量泛化能力有限（单智能体最多约13kg）。
- **评估指标单一**：仅使用成功率和平移精度，未考虑姿态自然度、协作效率（如完成时间）等。
- **潜在偏差**：运动数据来自AMASS数据集，可能未涵盖所有人类搬运策略，导致策略偏向特定模式。

（完）
