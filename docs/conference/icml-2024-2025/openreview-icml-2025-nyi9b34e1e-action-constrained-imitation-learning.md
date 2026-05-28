---
title: Action-Constrained Imitation Learning
title_zh: 动作约束模仿学习
authors: "Chia-Han Yeh, Tse-Sheng Nan, Risto Vuorio, Wei Hung, Hung Yen Wu, Shao-Hua Sun, Ping-Chun Hsieh"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=NYi9B34E1e"
tags: ["query:ur"]
score: 6.0
evidence: 提出用于动作约束模仿学习的替代数据集构建方法
tldr: 本文针对动作约束下的策略学习问题，提出DTWIL方法，通过轨迹对齐生成替代专家数据集，使模仿者能在满足自身动作约束的同时遵循状态轨迹。实验表明该方法有效解决了占用度不匹配问题，为机器人数据集构建提供了通用技术路线。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-nyi9b34e1e/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1679, \"height\": 430, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nyi9b34e1e/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 855, \"height\": 586, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nyi9b34e1e/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 792, \"height\": 401, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nyi9b34e1e/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 853, \"height\": 224, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nyi9b34e1e/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 840, \"height\": 462, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nyi9b34e1e/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1671, \"height\": 985, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nyi9b34e1e/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1028, \"height\": 534, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 716, \"height\": 542, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1727, \"height\": 698, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 651, \"height\": 242, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 668, \"height\": 243, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1304, \"height\": 167, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 821, \"height\": 330, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 675, \"height\": 237, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 652, \"height\": 169, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1418, \"height\": 320, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 901, \"height\": 206, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1345, \"height\": 329, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nyi9b34e1e/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 726, \"height\": 204, \"label\": \"Table\"}]"
motivation: 现有模仿学习在处理动作约束时存在专家与模仿者占用度不匹配的问题，需要构建合适的训练数据集。
method: 提出DTWIL框架，通过轨迹对齐将原始示范转换为符合动作约束的替代数据集，使模仿者学习。
result: 在多项控制任务上验证了DTWIL能有效提升动作约束下的策略性能。
conclusion: 提出了一套数据集构建方法，可广泛应用于机器人动作约束场景。
---

## Abstract
Policy learning under action constraints plays a central role in ensuring safe behaviors in various robot control and resource allocation applications.
In this paper, we study a new problem setting termed Action-Constrained Imitation Learning (ACIL), where an action-constrained imitator aims to learn from a demonstrative expert with larger action space.
The fundamental challenge of ACIL lies in the unavoidable mismatch of occupancy measure between the expert and the imitator caused by the action constraints. We tackle this mismatch through trajectory alignment and propose DTWIL, which replaces the original expert demonstrations with a surrogate dataset that follows similar state trajectories while adhering to the action constraints. Specifically, we recast trajectory alignment as a planning problem and solve it via Model Predictive Control, which aligns the surrogate trajectories with the expert trajectories based on the Dynamic Time Warping (DTW) distance. Through extensive experiments, we demonstrate that learning from the dataset generated by DTWIL significantly enhances performance across multiple robot control tasks and outperforms various benchmark imitation learning algorithms in terms of sample efficiency.

---

## 论文详细总结（自动生成）

# 论文《Action-Constrained Imitation Learning》中文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **研究动机**：在机器人控制和资源分配等安全关键场景中，策略学习必须在动作约束（如物理限制、安全边界）下进行。现有模仿学习通常假设专家与模仿者具有相同的动作空间，但在实际中专家可能拥有更灵活的动作集（例如人类演示），而模仿机器人受限于硬件约束（如扭矩上限、关节限位），导致专家示范无法直接复制。
- **定义新问题**：本文首次提出**动作约束模仿学习（ACIL）**——模仿者具有与专家不同的、更受限的动作空间，需要从专家示范中学习自身可执行的行为。
- **核心挑战**：由于动作约束，专家与模仿者之间的**占用度（occupancy measure）** 必然不匹配，即状态-动作分布不同，直接行为克隆或逆强化学习会导致策略失败。

## 2. 方法论：核心思想、关键技术细节
### 核心思想：轨迹对齐生成符合约束的替代数据集
- 不直接让模仿者学习原始专家轨迹，而是通过**轨迹对齐**将专家示范转换为**符合模仿者动作约束的替代轨迹**，使模仿者能跟踪相似的状态序列但使用自身动作。
- 将问题建模为**规划问题**：给定一条专家状态轨迹，寻找一条模仿者可行（满足动作约束）且与专家状态轨迹的动态时间规整（DTW）距离最小的模仿者轨迹。

### 关键技术细节（DTWIL框架）
1. **DTW距离**：用于衡量两条不同长度状态轨迹的相似性，通过非线性的时间对齐计算累积代价。
2. **模型预测控制（MPC）**：将轨迹对齐转化为一个带约束的最优控制问题。在每个时间步，MPC基于动态模型（如已知或已学习的动力学）规划未来一段时间的动作序列，目标是使受控轨迹与专家轨迹的DTW距离最小，同时满足动作约束（如动作边界）。
3. **替代数据集生成**：将每条专家示范经过MPC+DTW优化后，得到一条新的轨迹（状态-动作对），其状态序列与专家相似但动作完全在模仿者动作空间内。
4. **模仿学习**：使用生成的替代数据集训练模仿者策略（例如行为克隆或GAIL），此时占用度不匹配问题被缓解。

### 公式示意（文字说明）
- 优化目标：`min_{a_0..T} ∑_{i,j} w_{ij} * ||s_i (expert) - s_j (imitator)||²`，其中`w_{ij}`由DTW对齐决定，约束条件为`a_t ∈ A_imitator`。

## 3. 实验设计
- **测试场景**：多个连续控制任务，例如：
  - **Mujoco机器人**：如HalfCheetah、Hopper、Walker2d、Ant等，施加不同的动作约束（如关节限位或速度限制）。
  - **专用机器人**：如Sawyer机器人操作任务。
- **Benchmark**：非完全标准benchmark，而是自行设定不同动作约束条件（如限制专家动作范围的50%、30%等）。
- **对比方法**：
  - 直接行为克隆（BC）
  - 逆强化学习（如GAIL、AIRL）
  - 带约束的变体（如约束策略优化后模仿）
  - 以及一些轨迹对齐基线（如单纯使用欧几里得距离对齐）。
- **评估指标**：任务回报（reward）、样本效率、轨迹相似度（DTW距离）。

## 4. 资源与算力
- 论文**未明确说明**使用的GPU型号、数量或训练时长。
- 可通过实验规模推测：涉及多个Mujoco环境和Sawyer仿真，每次实验包含多随机种子，总计算量中等。但由于未提及，无法定量评估。

## 5. 实验数量与充分性
- **实验组数**：较为充分。包含：
  - 6个以上机器人控制任务的性能对比（见表2~5）。
  - 消融研究：分析DTW损失函数、MPC规划窗口长度、动态模型误差等影响。
  - 不同动作约束程度的对比（宽松/严格）。
  - 在不同随机种子下的统计结果（标准差/置信区间）。
- **充分性与公平性**：
  - 优点：对比了多种基线方法，包括直接训练和基于轨迹对齐的替代方法，设置了统一的评估流程。
  - 可能的不足：未在真实机器人上进行实物实验（仅在仿真），且动态模型假设为已知或易学，未充分验证模型偏差的影响。

## 6. 主要结论与发现
1. DTWIL能显著提升动作约束下模仿学习的性能，在大多数任务中优于直接模仿和现有算法。
2. 通过轨迹对齐生成的替代数据集有效解决了占用度不匹配问题，模仿者的状态轨迹与专家高度相似。
3. 样本效率高：在相同数据量下，DTWIL训练的策略回报更高。
4. DTW距离比欧几里得距离更适合处理不同长度和节奏的轨迹对齐。

## 7. 优点
- **问题新颖性**：首次系统定义动作约束模仿学习，并分析了占用度不匹配的根本原因。
- **方法论优雅**：将模仿学习转化为规划问题，通过MPC+DTW生成可行数据集，适用性强，不依赖特定模仿算法。
- **通用性**：生成数据集后可使用任意模仿学习算法，易于集成到现有框架。
- **实验设计**：多场景、多约束程度、消融实验较全面，有统计显著性。

## 8. 不足与局限
- **动态模型依赖**：MPC需要环境动力学模型（已知或学习），未知模型下误差可能累积。
- **计算开销**：每条专家轨迹需在线求解MPC，大规模数据集时计算成本高。
- **实验覆盖**：仅限于仿真环境，未在真实机器人上验证；任务主要为连续控制，未探索离散动作或高维视觉输入。
- **动作约束形式**：仅处理了数值边界约束（如扭矩/关节限位），未涉及复杂约束（如避障、接触力限制）。
- **风险偏差**：假设专家轨迹质量高，若专家示范本身次优，对齐可能引入偏差。

（完）
