---
title: "HumanVLA: Towards Vision-Language Directed Object Rearrangement by Physical Humanoid"
title_zh: HumanVLA：面向物理人形机器人的视觉语言指令物体重排
authors: "Xinyu Xu, Yizheng Zhang, Yong-Lu Li, Lei Han, Cewu Lu"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=pjD08dtAh0"
tags: ["query:ur"]
score: 6.0
evidence: 利用教师-学生框架进行人形机器人物体重排的大规模学习
tldr: 该论文提出HumanVLA，使真实人形机器人能够根据视觉语言指令进行物体重排。采用教师-学生框架：先通过强化学习训练状态基教师策略，再通过行为克隆蒸馏为视觉-语言-动作模型。该方法利用了大规模学习过程，其数据生成和训练范式对人形机器人数据集构建具有参考价值。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-pjd08dtah0/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1376, \"height\": 666, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pjd08dtah0/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1370, \"height\": 580, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pjd08dtah0/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1437, \"height\": 484, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pjd08dtah0/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1376, \"height\": 1084, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pjd08dtah0/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1426, \"height\": 789, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pjd08dtah0/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1015, \"height\": 751, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pjd08dtah0/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1009, \"height\": 761, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pjd08dtah0/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1384, \"height\": 646, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pjd08dtah0/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 668, \"height\": 480, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pjd08dtah0/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1162, \"height\": 810, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pjd08dtah0/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 717, \"height\": 487, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pjd08dtah0/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1303, \"height\": 1029, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-pjd08dtah0/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1364, \"height\": 402, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-pjd08dtah0/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1288, \"height\": 222, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-pjd08dtah0/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1290, \"height\": 754, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-pjd08dtah0/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1421, \"height\": 300, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-pjd08dtah0/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1423, \"height\": 277, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-pjd08dtah0/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1291, \"height\": 247, \"label\": \"Table\"}]"
motivation: 现有的人机交互技术局限于特定物体动力学和特权信息。
method: 教师-学生框架：先训练状态基教师策略，再蒸馏为视觉语言动作模型。
result: 实现了真实人形机器人根据自然语言指令重排物体。
conclusion: HumanVLA展示了结合视觉语言指令进行物理人形交互的潜力。
---

## Abstract
Physical Human-Scene Interaction (HSI) plays a crucial role in numerous applications. 
    However, existing HSI techniques are limited to specific object dynamics and privileged information, which prevents the development of more comprehensive applications.
    To address this limitation, we introduce HumanVLA for general object rearrangement directed by practical vision and language. 
    A teacher-student framework is utilized to develop HumanVLA.
    A state-based teacher policy is trained first using goal-conditioned reinforcement learning and adversarial motion prior.
    Then, it is distilled into a vision-language-action model via behavior cloning.
    We propose several key insights to facilitate the large-scale learning process.
    To support general object rearrangement by physical humanoid, we introduce a novel Human-in-the-Room dataset encompassing various rearrangement tasks.
    Through extensive experiments and analysis, we demonstrate the effectiveness of our approach.

---

## 论文详细总结（自动生成）

# HumanVLA 论文详细总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：现有的人机交互技术（HSI）主要局限于处理静态物体（如坐在椅子上）或特定物体动力学（如搬运箱子、抛球），缺乏对多样化物体（不同几何、姿态、重量）的通用操控能力。同时，已有方法依赖物体和目标的真实状态（特权信息）来指导人形机器人运动，难以在实际部署中获取，限制了应用潜力。
- **整体含义**：本文旨在开发一种由物理人形机器人执行通用物体重排任务的系统，能够通过**自然语言指令**和**第一人称视觉**感知环境，自主完成日常物体搬运、推动、拉拽等操作。这是向真实世界人形机器人应用迈出的重要一步，为未来通用型人形助手提供了基础。

## 2. 方法论：核心思想、关键技术细节

### 核心思想
采用**教师-学生（Teacher-Student）框架**，分两阶段训练：
- **第一阶段**：训练一个基于**特权状态**的教师策略（HumanVLA-Teacher），使用**目标条件强化学习**与**对抗运动先验（AMP）**，生成逼真且能完成任务的运动。
- **第二阶段**：通过**行为克隆**将教师策略蒸馏为**视觉-语言-动作模型（HumanVLA）**，仅依赖第一人称图像和自然语言指令，避免特权信息。

### 关键技术细节

#### 教师策略学习（状态基）
1. **强化学习框架**：以PPO算法优化累积奖励，奖励由任务奖励 \( r_G \) 和风格奖励 \( r_S \) 组成。风格奖励通过对抗判别器 \( D \) 从运动数据集中学习，公式为：
   \[
   r_S(s_{t+1}) = -\log(1 - D(s_{t+1-t^*:t+1}))
   \]
   判别器训练目标包含交叉熵损失和梯度惩罚。

2. **改进技术**：
   - **几何编码**：使用Basis Point Set (BPS)编码物体几何信息（如点云），使策略适应各种形状。
   - **搬运课程预训练（Carry Curriculum）**：先训练“走向物体+抓取并举起”两个步骤（搬运任务），再完整训练三个阶段（走向、接触、重新定位），降低长时任务难度。
   - **风格奖励裁剪**：将风格奖励上界设为当前任务奖励 \( r_G \) 与阈值 \( \xi_{\min} \) 的最大值，优先保证任务执行，避免模仿与任务冲突。
   - **上下文路径规划**：利用A*算法在2D占据地图上规划无碰撞路径，生成导航路标点引导运动。

#### 学生模型（VLA）训练
- **模型架构**：EfficientNet-B0编码图像，冻结的BERT编码语言，与本体感知和上一动作拼接后由6层MLP动作解码器输出28维关节目标位置。
- **行为克隆**：使用DAgger在线模仿学习，混合教师策略和当前学生策略探索环境，缓解协变量偏移。
- **主动渲染**：根据物体点云中心计算头部朝向，通过逆运动学生成颈部动作，使相机聚焦目标物体，提升感知质量。混合教师动作和主动渲染动作作为监督。

## 3. 实验设计

### 数据集与场景
- **Human-in-the-Room (HITR)**：包含四种房间布局（卧室、客厅、厨房、仓库），50个静态物体和34个可移动物体（尺寸21cm-126cm，重量5kg-20kg），共615个任务。任务由GPT-4-vision根据初始和目标场景图像生成自然语言指令，并经人工复核。
- **运动数据集**：OMOMO（包含7种物体的短程交互）和SAMP的行走子集，共约30分钟运动数据。

### Benchmark与对比方法
- **教师策略对比**：在箱子重排任务上与InterPhys（官方及其复现版）比较。
- **消融实验**：在训练集（552个任务）上分别去掉几何编码、搬运课程、风格裁剪、路径规划等组件。
- **视觉-语言模型对比**：对比无主动渲染、离线行为克隆（Offline GC-BC）的变体。
- **泛化实验**：在测试集（63个未见任务）上评估，包括场景、物体、指令均未见；额外分析未见文本、未见物体外观/几何、未见布局四种挑战。

### 评价指标
- **成功率**（Success Rate）：最终物体位置与目标距离小于阈值（状态基为20cm，VLA为40cm，因指令较粗糙）。
- **精度**（Precision）：平均最终距离（cm）。
- **执行时间**（Execution Time）：平均完成时间（秒）。

## 4. 资源与算力

- **教师策略训练**：在8块Tesla V100 GPU上训练约2天（16,384个并行环境，30,000 epoch）。
- **学生策略训练**：在2块GPU上训练约1天（585个环境，20,000 epoch）。
- 模拟器：IsaacGym，物理引擎60Hz，策略查询30Hz。

## 5. 实验数量与充分性

- **数量**：包含主实验、消融实验（5项教师策略组件、3项学生策略组件）、泛化实验（两种未见任务设置）、额外细分泛化分析（4种挑战）、定性可视化（多案例）。共计约10组定量实验和多个定性展示。
- **充分性与客观性**：
  - 消融覆盖了所有关键设计，验证每个组件的必要性。
  - 对比基准（InterPhys）为公开方法，且提供了官方和复现结果，公平性较好。
  - 使用10次重复运行报告统计显著性（教师策略标准差很小）。
  - 但教师策略与InterPhys的训练数据不同（HITR vs 原论文设置），直接比较时需谨慎，但论文已尽力对齐任务。
  - 未与更近期的VLA模型（如RT-2）比较，因为本文任务是整个人体重排，现有VLA模型主要针对机械臂，领域不同，可以理解。

## 6. 主要结论与发现

1. **教师策略**（HumanVLA-Teacher）在箱子重排上达到98.1%成功率、4.2cm精度，优于InterPhys（官方94.3%/8.3cm，复现97.8%/12.6cm）。
2. **消融实验**显示每个改进技术均显著提升性能：例如去掉几何编码成功率下降21.4%，去掉搬运课程下降19.6%，去掉路径规划下降18.1%，去掉风格裁剪下降6%。
3. **学生模型**（HumanVLA）在训练集上达到74.8%成功率（阈值40cm），无主动渲染时仅67.9%，无在线学习时仅15.3%。
4. **泛化性**：在未见任务上教师策略保持79.3%成功率（仅下降6.6%）；学生模型60.2%，虽显著下降但仍优于不主动渲染（56.7%）和离线BC（10.2%）。额外分析显示对未见文本和外观较鲁棒，但对未见物体几何和场景布局泛化较差（成功率20%-35%）。
5. **定性结果**展示人形机器人能成功推动桌子、搬运笔记本电脑、拉拽椅子等。

## 7. 优点

- **方法创新性**：首次将VLA模型应用于物理人形体完成通用物体重排，突破了以往仅支持静态或单物体交互的限制。
- **技术完整性**：从状态基强化学习到视觉语言蒸馏，涵盖了物理仿真、对抗模仿学习、课程学习、路径规划、主动感知等关键环节，形成完整流程。
- **数据集贡献**：HITR数据集包含多种家具、多房间布局，并生成自然语言指令，为后续研究提供了基准。
- **实验严谨**：对教师和学生进行多维度消融，报告统计显著性，并专门分析泛化失败案例，诚实指出局限性。
- **实用导向**：采用DAgger在线学习缓解协变量偏移，主动渲染提升感知质量，这些技巧对真实部署有借鉴意义。

## 8. 不足与局限

- **实验覆盖**：
  - 未与其他VLA模型（如RT-2、3D-VLA）在类似任务上比较，但这些模型主要面向桌面机械臂，并非直接公平对比。
  - 泛化测试中未见物体几何和场景布局时性能骤降（20%-35%），说明对视觉外观和物体形状的泛化能力有限。
- **偏差风险**：
  - 训练运动数据仅来自7种物体的交互，而HITR有34种可移动物体，数据分布可能存在偏差，导致对未见物体几何的泛化弱。
  - 语言指令由GPT-4生成并人工修正，但训练集中的指令可能具有特定模式，测试集中若出现更复杂句式可能失败。
- **应用限制**：
  - 人形模型使用球形手，无法精细操作小物体。
  - 每任务仅移动一个物体，缺乏长时多物体交互能力。
  - 未集成显式记忆、规划、导航和协作模块，复杂场景下可能表现不佳。
  - 仅仿真环境验证，未在真实人形机器人上实验，仿真到现实的迁移问题未解决。
- **算力需求**：教师训练需要8块V100 GPU连续2天，资源消耗较大，可能限制可复现性。

（完）
