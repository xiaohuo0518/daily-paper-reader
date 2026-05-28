---
title: "HumanoidGen: Data Generation for Bimanual Dexterous Manipulation via LLM Reasoning"
title_zh: HumanoidGen：利用LLM推理生成双臂灵巧操作数据
authors: "Zhi Jing, Siyuan Yang, Jicong Ao, Ting Xiao, Yu-Gang Jiang, Chenjia Bai"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=Mk9ykil8eP"
tags: ["query:ur"]
score: 9.0
evidence: 直接为仿人机器人生成双臂灵巧操作数据集，满足仿人机器人数据集构建需求
tldr: 现有操作数据集主要面向机器人臂平台，缺乏仿人双臂灵巧操作的高质量演示。本文提出HumanoidGen框架，利用大语言模型（LLM）的推理能力，结合原子灵巧操作和空间标注，自动创建任务并收集演示。框架基于关系约束生成多样化任务，并产出配对的视觉-动作数据。实验表明，生成的数据集可有效训练仿人机器人操作策略，填补了仿人机器人数据集构建的空白。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-mk9ykil8ep/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1448, \"height\": 617, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mk9ykil8ep/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1455, \"height\": 339, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mk9ykil8ep/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1295, \"height\": 1144, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mk9ykil8ep/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1444, \"height\": 489, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mk9ykil8ep/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1414, \"height\": 496, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mk9ykil8ep/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 726, \"height\": 425, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mk9ykil8ep/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1446, \"height\": 340, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mk9ykil8ep/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1444, \"height\": 396, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mk9ykil8ep/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1442, \"height\": 283, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mk9ykil8ep/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1244, \"height\": 1197, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mk9ykil8ep/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1445, \"height\": 346, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mk9ykil8ep/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1435, \"height\": 451, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mk9ykil8ep/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1402, \"height\": 802, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-mk9ykil8ep/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1388, \"height\": 2230, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-mk9ykil8ep/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 660, \"height\": 484, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mk9ykil8ep/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1443, \"height\": 783, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mk9ykil8ep/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1445, \"height\": 983, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mk9ykil8ep/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1444, \"height\": 358, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mk9ykil8ep/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1429, \"height\": 148, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mk9ykil8ep/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1388, \"height\": 176, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mk9ykil8ep/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1462, \"height\": 150, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mk9ykil8ep/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1457, \"height\": 147, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mk9ykil8ep/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1445, \"height\": 329, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mk9ykil8ep/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1441, \"height\": 1863, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mk9ykil8ep/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1444, \"height\": 267, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-mk9ykil8ep/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1443, \"height\": 578, \"label\": \"Table\"}]"
motivation: 仿人机器人双臂灵巧操作缺乏高质量仿真任务和数据集。
method: 结合原子灵巧操作和LLM推理，生成关系约束并自动化任务创建与演示收集。
result: 生成了多样化的仿人机器人操作数据集，成功用于训练操作策略。
conclusion: HumanoidGen为仿人机器人数据集构建提供了自动化解决方案，促进了双臂灵巧操作研究。
---

## Abstract
For robotic manipulation, existing robotics datasets and simulation benchmarks predominantly cater to robot-arm platforms. However, for humanoid robots equipped with dual arms and dexterous hands, simulation tasks and high-quality demonstrations are notably lacking. Bimanual dexterous manipulation is inherently more complex, as it requires coordinated arm movements and hand operations, making autonomous data collection challenging. This paper presents HumanoidGen, an automated task creation and demonstration collection framework that leverages atomic dexterous operations and LLM reasoning to generate relational constraints. Specifically, we provide spatial annotations for both assets and dexterous hands based on the atomic operations, and perform an LLM planner to generate a chain of actionable spatial constraints for arm movements based on object affordances and scenes. To further improve planning ability, we employ a variant of Monte Carlo tree search to enhance LLM reasoning for long-horizon tasks and insufficient annotation. In experiments, we create a novel benchmark with augmented scenarios to evaluate the quality of the collected data. The results show that the performance of the 2D and 3D diffusion policies can scale with the generated dataset. Project page is https://openhumanoidgen.github.io.

---

## 论文详细总结（自动生成）

## 论文详细中文总结

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **问题**：现有机器人操作数据集和仿真基准主要面向传统单臂或双臂但不含灵巧手的机器人平台。对于配备双臂和灵巧手的仿人机器人，高质量、多样化的仿真任务和演示数据严重缺乏。
- **挑战**：双臂灵巧操作需要协调的手臂运动与手指精细动作，数据收集极其困难。传统遥操作（VR、外骨骼）成本高、效率低，难以覆盖多种场景。
- **动机**：利用大语言模型（LLM）的推理能力，实现自动化任务创建和演示收集，以解决仿人机器人数据稀缺问题，推动双臂灵巧操作研究。  

### 2. 论文提出的方法论

#### 核心思想
- **原子灵巧操作 + LLM推理**：预先定义灵巧手的基本原子操作（如捏、抓、按），并对资产（物体）和手进行空间标注（关键点与轴）。利用LLM进行任务分解，生成一系列关系约束（point/axis coincidence, parallelism等），然后通过轨迹优化器求解约束得到具体手臂和手指的运动，从而自动收集演示数据。

#### 关键技术细节
1. **空间标注**：
   - 手部原子操作标注：每种原子操作定义三个轴（approach axis, attach axis, parallel axis）和相关关键点。
   - 资产固有信息：关键点和轴，表明资产功能（如杯子的倾倒点和存储点）。
   - 资产操作标注：指示如何通过不同原子操作与资产交互（一个资产可支持多种操作）。
2. **场景生成**：LLM根据任务描述、资产库和场景信息，生成环境设置代码（资产类别、数量、位姿）和任务成功条件。
3. **任务规划**：
   - **任务分解**：LLM将长时任务分解为动作序列 `S = {S1, S2, ..., Sn}`，每步包含左手和右手操作（原子操作或手臂移动）。手臂移动定义两类约束：目标约束 C_goal 和路径约束 C_path。
   - **关系动作约束**：引入动态作用帧 F_act，包含关键点和轴。约束形式包括点重合、平行等，用于编码空间逻辑。
   - **碰撞避免**：主动碰撞避免（LLM生成脚本时预先规划避碰）和动态碰撞管理（LLM动态调整忽视列表，允许接触时忽略碰撞，自由运动时恢复检测）。
4. **MCTS增强推理**：
   - **STCR机制**：将执行代码分段（Segment）、在失败点截断（Truncate）、合并意图一致的操作（Combine）、存储关键信息用于恢复（Resume），构建搜索树。
   - **MCTS**：结合选择（基于折扣UCB）、扩展（调用LLM生成新代码）、反向传播（基于“有价值时刻”的内在奖励）。显著提升长时任务和标注不足情况下的推理能力。
5. **场景缩放**：通过坐标变换将桌面级任务扩展到房间级场景，增加数据多样性。
6. **数据收集**：执行生成的约束脚本，通过轨迹优化器（SNOPT + mplib）求解手臂和手部动作，记录成功轨迹。

#### 算法流程（文字描述）
1. 预处理：对资产和灵巧手进行空间标注。
2. 场景生成：LLM产生环境代码，搭建初始场景。
3. 任务部署：LLM生成约束链。
4. MCTS推理（可选）：针对复杂/长时任务，通过MCTS探索改进规划。
5. 轨迹优化：求解约束得到手臂和手指的关节运动。
6. 执行验证：在仿真器中执行并记录成功轨迹。
7. 场景缩放：推广到更多场景。

### 3. 实验设计

- **数据集/场景**：自行构建的 **HGen-Bench** 基准，包含20个桌面级双臂灵巧操作任务，使用Unitree H1-2人形机器人+Inspire灵巧手（双臂各7自由度，每只手6自由度，共26维动作空间），基于SAPIEN仿真器。场景包含多种物体（方块、铰接物体如抽屉、笔记本、日常用品如杯子、盘子等），并设置随机初始位姿和关节角度。
- **对比方法**：将RoboTwin修改为支持灵巧手并进行对比。此外，消融实验对比了非MCTS版本。
- **评估指标**：任务成功率（数据生成阶段）、策略学习成功率（DP和DP3在不同数据量下的表现）。

### 4. 资源与算力

- 文中未明确说明所使用的GPU型号、数量、训练时长等具体硬件信息。仅在附录C.4提供了各阶段的平均时间和LLM token消耗，但未提及GPU。仅提及使用DeepSeek-R1作为LLM。

### 5. 实验数量与充分性

- **数据生成实验**（§5.1）：20个任务分为4组，对比HumanoidGen与RoboTwin，每组重复多次（有标准差），展示了成功率。
- **MCTS消融实验**（§5.2）：4个任务（blocks stack single, blocks stack easy/hard, pyramid stack），比较MCTS与非MCTS，统计成功率和token消耗，记录不同探索步数的影响。
- **策略学习实验**（§5.3）：14个任务，使用3种数据量（20/50/100个演示），训练DP和DP3，每个配置3个随机种子，报告成功率的均值和标准差。
- **额外实验**（附录）：真实世界实验（2个任务，评估sim2real转移）、自动标注评估、其他大模型对比、额外挑战任务等。
- **评估充分性**：实验覆盖了数据生成、推理增强、策略学习、消融等多方面，统计了误差，结果可信。但对比基线较少（仅RoboTwin），缺少与RoboGen、Gensim等系统级生成框架的全面对比；DP/DP3在某些长时任务上完全失败，说明数据或策略仍有局限。

### 6. 论文的主要结论与发现

1. HumanoidGen在数据生成成功率上显著优于RoboTwin，尤其在长时程、复杂碰撞任务中（平均成功率>50%，多数任务>75%）。
2. MCTS显著提升了LLM在复杂任务（标注不足、长时程）下的推理能力，额外token消耗较少，且能产生更多样化的成功计划。
3. 生成的数据可用于训练扩散策略（DP和DP3），且随着数据量增加策略性能持续提升（少数任务表现出few-shot学习能力）。
4. 动态碰撞管理有效改善了轨迹规划的灵活性。

### 7. 方法或实验设计上的优点

- **自动化程度高**：无需人工遥操作，完全由LLM驱动任务创建和演示收集。
- **空间标注精细**：为灵巧手和资产定义了关键点和轴，使LLM能够进行精细的空间推理，生成可执行的约束。
- **碰撞管理灵活**：LLM动态控制碰撞检测列表，兼顾接触操作和自由运动，减少了手动调试。
- **MCTS增强推理**：针对复杂推理场景，通过搜索和回溯提升成功率，且token消耗高效。
- **场景缩放**：从桌面到房间级场景的自动转换增加了数据多样性。
- **真实世界验证**：附录中展示了sim2real转移实验，验证了方法的部分可行性。

### 8. 不足与局限

- **仍需人工干预**：新资产类别初次出现时需要人工标注关键点和轴，无法完全自动。
- **物理引擎限制**：不支持变形物体、流体等任务；依靠运动规划器，难以处理需要连续调整的模糊目标任务（如推物体、布料操作）。
- **策略学习局限**：生成的数据在部分长时、精细任务上不足以让DP/DP3学会有效策略（如Handover and Storage、Blocks Stack Hard成功率为0）。
- **对比不足**：仅与RoboTwin对比，未与RoboGen、Gensim等更全面的框架进行系统比较。
- **仿真到现实的迁移**：虽有初步真实世界实验，但未大规模验证数据对真实策略的泛化能力。
- **计算资源未明确**：未报告GPU型号、数量、总训练时间，影响复现性。

（完）
