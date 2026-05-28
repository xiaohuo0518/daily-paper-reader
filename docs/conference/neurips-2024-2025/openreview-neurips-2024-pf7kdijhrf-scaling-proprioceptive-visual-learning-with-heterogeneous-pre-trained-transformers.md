---
title: Scaling Proprioceptive-Visual Learning with Heterogeneous Pre-trained Transformers
title_zh: 利用异构预训练变换器扩展本体感知-视觉学习
authors: "Lirui Wang, Xinlei Chen, Jialiang Zhao, Kaiming He"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=Pf7kdIjHRf"
tags: ["query:ur"]
score: 5.0
evidence: 跨本体的机器人异构数据预训练
tldr: 当前机器人学习受限于针对特定本体和任务的数据收集，昂贵且易过拟合。本文提出异构预训练变换器（HPT），在来自不同本体和任务的机器人数据上预训练一个大型共享网络主干，学习与任务和本体无关的共享表征。该架构将具体的本体感知和视觉输入对齐为短序列令牌并处理。实验表明HPT在下游任务中表现出更好的泛化性能。该方法为利用大规模异构机器人数据集提供了有效范式。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 685, \"height\": 358, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 768, \"height\": 606, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1437, \"height\": 366, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 609, \"height\": 440, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1413, \"height\": 438, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1415, \"height\": 478, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 676, \"height\": 654, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1428, \"height\": 305, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1448, \"height\": 228, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 967, \"height\": 319, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 845, \"height\": 275, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1394, \"height\": 662, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1449, \"height\": 249, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1429, \"height\": 274, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1383, \"height\": 306, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1417, \"height\": 387, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1335, \"height\": 216, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 654, \"height\": 336, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pf7kdijhrf/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 726, \"height\": 326, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-pf7kdijhrf/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 727, \"height\": 211, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-pf7kdijhrf/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 728, \"height\": 140, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-pf7kdijhrf/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 557, \"height\": 348, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-pf7kdijhrf/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1025, \"height\": 1376, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-pf7kdijhrf/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1145, \"height\": 243, \"label\": \"Table\"}]"
motivation: 机器人学习面临数据异构性问题，针对特定本体收集数据成本高且易过拟合。
method: 提出异构预训练变换器HPT，在大规模异构机器人数据上预训练共享表征。
result: HPT在下游多种任务和本体上展现出更好的泛化能力和数据效率。
conclusion: HPT验证了跨本体异构预训练的有效性，为通用机器人策略学习奠定基础。
---

## Abstract
One of the roadblocks for training generalist robotic models today is heterogeneity. Previous robot learning methods often collect data to train with one specific embodiment for one task, which is expensive and prone to overfitting. This work studies the problem of learning policy representations through heterogeneous pre-training on robot data across different embodiments and tasks at scale. We propose Heterogeneous Pre-trained Transformers (HPT), which pre-train a large, shareable trunk of a policy neural network to learn a task and embodiment agnostic shared representation. This general architecture aligns the specific proprioception and vision inputs from distinct embodiments to a short sequence of tokens and then processes such tokens to map to control robots for different tasks. Leveraging the recent large-scale multi-embodiment real-world robotic datasets as well as simulation, deployed robots, and human video datasets, we investigate pre-training policies across heterogeneity. We conduct experiments to investigate the scaling behaviors of training objectives, to the extent of 52 datasets. HPTs outperform several baselines and enhance the fine-tuned policy performance by over 20% on unseen tasks in multiple simulator benchmarks and real-world settings. See the project website (liruiw.github.io/hpt) for code and videos.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：机器人学习面临严重的**异构性**挑战——不同机器人本体（embodiment）具有不同的传感器（视觉、本体感知）、自由度、动作空间和控制频率。传统方法针对每个特定本体和任务单独收集数据，成本高昂且易过拟合，导致学到的策略无法泛化到新场景。
- **整体含义**：本文借鉴自然语言处理和计算机视觉中的预训练范式（如大规模语言模型、视觉基础模型），尝试利用大规模、多样化的异构机器人数据预训练一个**任务无关、本体无关的共享表征**，以降低对新本体的数据需求并提升泛化能力。该工作旨在为构建通用机器人基础模型（robotic foundation model）奠定方法基础。

## 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

### 核心思想
- 提出**异构预训练变换器（Heterogeneous Pre-trained Transformers, HPT）**，将机器人策略网络模块化为三部分：**Stem（茎）**、**Trunk（主干）**、**Head（头）**。其中Trunk在大量异构数据上共享预训练，学习与任务和本体无关的潜表征；Stem负责将不同本体的感知输入（本体感知和视觉）对齐为固定数量的令牌（tokens）；Head将Trunk输出的表征映射到具体动作空间。

### 关键技术细节
- **Stem架构**（图3）：
  - **本体感知令牌化**：首先用MLP将本体感知信息映射到d维特征，然后通过交叉注意力机制（cross-attention）将可学习令牌（默认16个）与特征交互，输出固定数量令牌。
  - **视觉令牌化**：使用预训练冻结的视觉编码器（如ResNet18）提取图像特征，再通过交叉注意力将可学习令牌（默认16个）压缩为固定数量令牌。
  - 两种令牌拼接后加入模态编码和位置编码，作为Trunk的输入序列。Stem参数极少（一个MLP+一个注意力层），防止过拟合。
- **Trunk架构**：标准Transformer（decoder-only），宽度从128到1024，深度从16到80层，参数量从3.1M到1.1B。Trunk在所有异构数据上共享，输出令牌序列经池化后作为观测的联合特征。
- **Head架构**：可以是简单的MLP、Transformer decoder或扩散策略（diffusion policy），将Trunk的输出映射到归一化动作。每个任务/本体有独立的Head，在预训练和微调时重新初始化。
- **训练目标**（公式1）：
  \[
  \min_{\theta} \sum_{k=1}^{K} \mathcal{L}(\theta_{\text{stem}^k}, \theta_{\text{trunk}}, \theta_{\text{head}^k}; \mathcal{D}_k)
  \]
  其中 \(\mathcal{L}\) 为行为克隆损失（Huber Loss），对归一化动作标签与预测动作计算损失。\(\theta_{\text{stem}^k}\) 和 \(\theta_{\text{head}^k}\) 为数据集k专属参数，\(\theta_{\text{trunk}}\) 为所有数据集共享参数。

### 算法流程（文字描述）
1. **预训练阶段**：从K个异构数据集中采样批次，每个批次激活对应本体的Stem和Head，共享Trunk接收所有批次梯度更新。使用AdamW优化器，余弦学习率调度，批次大小随数据规模增大。
2. **迁移学习阶段**：给定新本体数据集，重新初始化其Stem和Head（适配输入输出维度），冻结预训练Trunk权重，使用相同或自定义的行为克隆损失进行微调（也可选择端到端微调整个网络）。

## 3. 实验设计

### 使用数据集
- **默认设置**：27个真实机器人遥操作数据集（来自Open X-Embodiment子集），每个数据集最多1000条轨迹，共约16k轨迹。
- **扩展设置**：52个数据集（包括额外的仿真、部署机器人、人类视频数据），共约270k轨迹。
  - 仿真数据集：Drake, Mujoco (Meta-world, RoboMimic), Isaac Sim, PyBullet, Sapien, Flex等（7个）。
  - 人类视频数据集：EPIC-Kitchen, PoCo（使用手部姿态或2D位置作为伪动作）。
  - 部署机器人数据集：FrodoBots-2K（野外驾驶机器人）。
- **验证集**：每个数据集最多200条保留轨迹。

### Benchmark / 评估环境
- **预训练评估**：使用平均验证损失（prediction error）衡量预训练进度。
- **下游任务评估**：
  - **仿真**：Meta-world (10个任务), RoboMimic, Fleet-Tools, Simpler benchmark（Google EDR任务：关门、靠近、拿可乐罐）。
  - **真实世界**：两个机器人本体，四项任务（扫除剩余物、倒水、舀食物、开关插入），每任务约100个人工示教，评估15次试次。

### 对比方法
- **预训练阶段**：无Trunk（仅Stem+Head）、从头训练（From Scratch）、预训练冻结（Pretrained Frozen）、预训练微调（Pretrained Finetuned）、不同规模模型（HPT-Base/XL等）。
- **真实世界对比**：R3M、Voltron、VC-1（仅预训练视觉编码器）、无本体感知预训练（No Prop.）、不同模型规模（HPT-B/XL）。
- **Simpler benchmark对比**：Octo、RT-1-X、RT-2-X（来自论文结果）。

## 4. 资源与算力

- **计算资源**：
  - 预训练实验使用 **8 V-100 到 128 V-100 GPU**（具体取决于实验规模）。
  - 训练时长从 **半天到一个月**（最大模型约1.1B参数，训练约0.65B潜空间令牌）。
  - 默认预训练：80k迭代，batch size 256（约0.65B令牌）。
  - 真实世界微调：单张RTX 2080Ti GPU上训练约4小时（20000迭代）。
- **推理速度**：HPT-Base在RTX 3070上约47Hz，HPT-XL约19Hz；A100上快3-4倍。
- **数据存储**：总数据集约10TB，RAM要求低于50GB。

## 5. 实验数量与充分性

- **预训练缩放实验**（图5-8）：
  - 数据量缩放：从每个数据集10条轨迹（共270）到100000条（共170k），验证损失持续下降。
  - 数据集数量缩放：从10到52个数据集，模型规模从HPT-S到HPT-XL，多组重复实验（4次）。
  - 模型规模缩放：从1M到1B参数，逐步增加batch size和数据，验证损失降低。
  - Epoch缩放：增加训练令牌（batch size × 迭代数）改善性能。
  - 额外数据集：加入仿真和人类视频数据后验证损失优于仅用真实数据。
- **迁移学习实验**（图10, 12, 表3）：
  - 仿真：在Meta-world, RoboMimic, Fleet-Tools上比较无Trunk、从头训练、预训练冻结/微调，每个条件5次独立运行取平均。
  - Simpler benchmark：218个episode（3个任务，不同初始化），与Octo等对比。
  - 真实世界：4个任务，每个模型15 trials，报告平均值和标准差。
  - 消融实验：对比R3M、Voltron、VC-1（表3）；比较有无本体感知预训练；不同模型规模。
- **充分性**：实验覆盖数据量、模型大小、训练epoch、数据集多样性、跨领域（仿真、真实、人类视频）的缩放行为；下游任务覆盖多种仿真benchmark和真实任务；消融实验包括关键设计选择（本体感知/视觉有无、视觉编码器、头架构）。作者承认一些局限性（如评估限于短视距操作任务、成功率未达90%），但整体实验较为充分、客观，使用多次运行和标准差报告。

## 6. 论文的主要结论与发现

1. **HPT预训练具有缩放行为**：随着数据量（轨迹数、数据集数）、模型大小（1M到1B参数）和计算量增加，验证损失持续降低，类似NLP中的缩放定律。
2. **异构数据有助于泛化**：在更多不同本体（仿真、人类视频、部署机器人）上的预训练可进一步提升表征质量（即使这些数据与下游任务差异大）。
3. **迁移学习显著提升性能**：HPT预训练表示在未见过的任务和本体上，相比于从零训练或仅视觉预训练方法，成功率提升超过20%（仿真和真实世界均验证）。
4. **本体感知和视觉联合预训练更优**：同时使用本体感知和视觉信息进行预训练，效果优于只预训练视觉编码器（如R3M、VC-1）后再加入本体感知的做法。
5. **模块化架构有效**：固定令牌长度的Stem + 共享Trunk + 任务特定Head的设计可以灵活处理异构输入，且微调参数极少（仅2%）。

## 7. 优点

- **创新性**：首次系统研究跨本体（包括真实机器人、仿真、人类视频）的**联合本体感知-视觉预训练**，提出模块化架构解决异构性对齐问题。
- **架构设计优雅**：使用交叉注意力将任意维度的感知输入压缩为固定数量令牌，使共享Trunk可统一处理异构数据；Stem参数极少避免过拟合。
- **缩放分析全面**：对数据量、模型大小、计算量、异构程度进行了多维度缩放实验，揭示预训练行为规律，类似LLM领域的缩放定律研究。
- **开源与可复现**：开源代码和模型权重，提供详细实现细节（附录），利于社区跟进。
- **跨领域验证**：在仿真（多种benchmark）和真实世界（两个不同本体、四项复杂任务）中均验证，且与多种基线公平比较（包括扩散策略、泛化策略Octo等）。

## 8. 不足与局限

- **数据集混合与质量**：数据集的采样权重仅使用简单的平衡策略，未深入探究最佳混合比例；数据清洗和过滤工作不足（文中提及）。
- **预训练收敛慢**：异构数据方差大，模型收敛速度较慢（需要大batch size和大量迭代）。
- **评估任务局限性**：下游迁移学习仅限于短视距操作任务（~5-20秒），未涉及长时域任务或移动操作；成功率仍低于90%（常见低于80%），可靠性不足。
- **闭环性能gap**：主要使用验证损失（open-loop prediction error）进行预训练评估，未完全证明其与闭环任务成功率的强相关性（作者承认这一点）。
- **缺乏语言/多模态对齐**：默认设置未利用语言指令（虽然提到可扩展），主要依赖视觉和本体感知；在需要语言条件化的任务（如Simpler benchmark）中需额外处理。
- **失败模式**：真实世界实验中存在过冲/欠冲问题（如倒水未对准），主要由数据质量和空间精度引起（附录C）。
- **计算成本**：最大模型1.1B参数，训练需要大量GPU资源（128 V-100，月级别），对小型研究团队门槛较高。

（完）
