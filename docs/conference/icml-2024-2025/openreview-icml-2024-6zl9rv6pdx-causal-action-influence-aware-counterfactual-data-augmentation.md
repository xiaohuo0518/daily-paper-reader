---
title: Causal Action Influence Aware Counterfactual Data Augmentation
title_zh: 因果动作影响感知的反事实数据增强
authors: "Núria Armengol Urpí, Marco Bagatella, Marin Vlastelica, Georg Martius"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=6Zl9rv6PDx"
tags: ["query:ur"]
score: 7.0
evidence: 从离线机器人数据集创建合成转换的反事实数据增强
tldr: 本文提出CAIAC，一种基于因果影响量化的反事实数据增强方法，无需环境交互即可从固定离线数据集生成可行的合成转换。该方法避免了伪相关，提高了机器人策略的泛化能力。在多个机器人任务中验证了其有效性，为构建更丰富的数据集提供了新思路。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-6zl9rv6pdx/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 863, \"height\": 480, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-6zl9rv6pdx/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 864, \"height\": 441, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-6zl9rv6pdx/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1748, \"height\": 486, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-6zl9rv6pdx/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 858, \"height\": 399, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-6zl9rv6pdx/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1545, \"height\": 395, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-6zl9rv6pdx/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1370, \"height\": 438, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-6zl9rv6pdx/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 637, \"height\": 399, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-6zl9rv6pdx/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1780, \"height\": 705, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-6zl9rv6pdx/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1031, \"height\": 378, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-6zl9rv6pdx/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 518, \"height\": 519, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-6zl9rv6pdx/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1784, \"height\": 608, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-6zl9rv6pdx/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1785, \"height\": 610, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-6zl9rv6pdx/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1559, \"height\": 395, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-6zl9rv6pdx/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 867, \"height\": 338, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-6zl9rv6pdx/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 857, \"height\": 271, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-6zl9rv6pdx/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 832, \"height\": 152, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-6zl9rv6pdx/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 930, \"height\": 149, \"label\": \"Table\"}]"
motivation: 离线数据集有限且存在伪相关，需要数据增强提升策略泛化。
method: 量化动作的因果影响，对动作无关状态进行反事实替换生成合成数据。
result: 在多个机器人控制任务上显著提升了策略性能和鲁棒性。
conclusion: 因果驱动的数据增强能有效扩充机器人数据集，提升学习效率。
---

## Abstract
Offline data are both valuable and practical resources for teaching robots complex behaviors. Ideally, learning agents should not be constrained by the scarcity of available demonstrations, but rather generalize beyond the training distribution. However, the complexity of real-world scenarios typically requires huge amounts of data to prevent neural network policies from picking up on spurious correlations and learning non-causal relationships. We propose CAIAC, a data augmentation method that can create feasible synthetic transitions from a fixed dataset without having access to online environment interactions. By utilizing principled methods for quantifying causal influence, we are able to perform counterfactual reasoning by swapping $\textit{action}$-unaffected parts of the state-space between independent trajectories in the dataset. We empirically show that this leads to a substantial increase in robustness of offline learning algorithms against distributional shift.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **核心问题**：在离线强化学习（offline RL）和模仿学习中，策略容易受到训练数据中**伪相关（spurious correlation）** 的干扰，导致**因果混淆（causal confusion）**。当测试环境出现分布偏移（distributional shift）时，策略常常发生灾难性失败。
- **背景**：现实机器人演示数据往往只覆盖了少量状态组合，例如在厨房环境中，机器人打开微波炉时，另一个滑动柜门总是处于某种状态。策略可能错误地学习到“滑动柜门打开”是执行某个动作的必要条件，从而在微波炉关闭时无法完成滑动柜门任务。
- **研究目标**：提出一种无需在线环境交互的**反事实数据增强方法**，生成可行（feasible）的合成转换样本，扩大联合状态空间的覆盖范围，使策略对分布外场景具有更强的鲁棒性。

## 2. 论文提出的方法论
### 2.1 核心思想
- 利用**局部因果图（Local Causal Model）** 思想，在给定当前状态 $s$ 时，动作 $a$ 对某些实体（entity）的状态下一时刻 $s'_j$ 没有因果影响（即 $A \not\to S'_j$）。这些实体称为**动作不可控实体（uncontrollable set $U_s$）**。
- 假设环境中**实体间相互作用稀疏**（例如机器人厨房中各物体几乎不会互相影响），从而将全因果图的发现问题简化为**动作影响检测**问题。
- 通过在不同轨迹中**交换不可控实体的状态**，创建反事实样本：给定两个转换 $(s, a, s')$ 和 $(\hat{s}, \hat{a}, \hat{s}')$，若某个实体 $i$ 在两个状态中都属于不可控集，则将 $(s_i, s'_i)$ 与 $(\hat{s}_i, \hat{s}'_i)$ 交换，得到新的转换 $(\tilde{s}, a, \tilde{s}')$。

### 2.2 关键技术细节
- **因果动作影响（CAI）**：使用以状态为条件的互信息（conditional mutual information）作为度量：
  $$
  C_j(s) := I(S'_j; A \mid S=s) = \mathbb{E}_{a\sim\pi}\left[ D_{KL}\left( P_{S'_j|s,a} \parallel P_{S'_j|s} \right) \right]
  $$
  其中 $P_{S'_j|s,a}$ 用一个高斯神经网络建模（预测均值和方差），$P_{S'_j|s}$ 通过对 $M$ 个动作样本的边缘化得到。
- 阈值 $\theta$：$C_j(s) \le \theta$ 则判定 $s_j$ 为不可控实体。
- 对于时间窗口 $\kappa > 1$（如技能学习），不可控集取交集：$U_{t:t+\kappa} = \bigcap_{\tau=t}^{t+\kappa-1} U_{s_\tau}$。

### 2.3 算法流程（文字说明）
1. 从离线数据集 $D$ 中训练 CAI 模型（即状态条件转移模型）。
2. 对 $D$ 中每个状态 $s$，计算每个实体的 $C_j(s)$，根据阈值 $\theta$ 得到不可控集 $U_s$。
3. 在训练下游策略时，每次采样一个原始转换 $(s, a, s')$，对于其中每个不可控实体 $s_i$，从数据集中随机采样另一个转换 $(\hat{s}, \hat{a}, \hat{s}')$，若对应实体 $i$ 也在其不可控集中，则交换该实体的状态，生成反事实样本 $(\tilde{s}, a, \tilde{s}')$。
4. 将原始样本和反事实样本以一定比例混合用于策略训练。

## 3. 实验设计
### 3.1 使用场景和数据集
- **Franka-Kitchen**（D4RL）：7-DoF 机器人臂操作厨房物品（微波炉、水壶、开关等）。数据集包含专家演示，但存在固有伪相关（例如微波炉打开时滑动柜门总是打开）。
  - 简化版本（Motivating Experiment）：仅保留微波炉和水壶任务，人为制造伪相关。
  - 完整版本（All Tasks）：使用所有 6 个任务，测试时随机初始化非目标实体的状态，模拟分布外。
- **Fetch-Push**（两方块）：机器人手臂将两个方块推到目标位置。数据量分为 20K 和 4K（低数据 regime）。
- **Fetch-Pick&Lift**（四方块）：机器人捡起并抬起目标方块。训练时所有方块排成一条线，测试时随机放置。

### 3.2 基准方法
- **No Augmentation**：不使用数据增强。
- **CoDA**（Pitis et al., 2020）：使用 Transformer 注意力权重估计局部因果图，然后交换连接组件。
- **CoDA-action**：CoDA 的变体，仅估计动作的影响。
- **RSC**（Ding et al., 2023）：通过启发式扰动状态并学习结构因果模型预测下一状态。
- **MBPO**（模型基线）：训练动力学模型并生成 rollout 数据。
- **CAIAC+MBPO**：结合 CAIAC 增强数据训练动力学模型，再使用 MBPO。

### 3.3 下游学习算法
- Franka-Kitchen：**LMP**（Latent Plan from Play），一个离线目标条件技能学习算法。
- Fetch 环境：**TD3+BC**（离线 RL）结合 HER 目标重标定。

## 4. 资源与算力
- **论文未明确说明使用的 GPU 型号、数量或训练时长**。
- 只提供了计算反事实生成时间的评估（Table 2）：在 12 核 Intel i7 CPU 上，CAIAC 约 13 分钟处理 2M 数据点，CoDA 约 10 分钟，CoDA-action 约 119 分钟。
- 下游策略训练的具体算力未报告。

## 5. 实验数量与充分性
- **实验数量**：涵盖 3 个主要环境（Franka-Kitchen 简化版、完整版、Fetch-Push、Fetch-Pick&Lift），总共约 10+ 组不同设置（包括不同数据量、OOD 场景、不同比例 counterfactual 消融等）。
- **消融实验**：
  - 不同 counterfactual 比例（0.0~1.0）对性能的影响（图 6）。
  - 不同阈值 $\theta$ 的 ROC 曲线分析（图 10-12）。
  - 生成样本的质量评估：可行性与支持覆盖（图 2、Table 3）。
- **充分性**：实验设计较为全面，涵盖 OOD 和低数据两种关键挑战，对比了多种 baseline，并进行了统计显著性（置信区间）。但在某些任务（如 hinge cabinet）所有方法都失败，说明挑战性很大，但并未深入分析原因。实验总体客观公平，阈值通过网格搜索优化。

## 6. 主要结论与发现
- **CAIAC 显著提升了策略在分布外（OOD）场景下的成功率**，尤其是在 Franka-Kitchen 和 Fetch-Pick&Lift 任务中，远超所有 baseline。
- **CAIAC 生成的样本具有高可行性**（符合环境真实动力学），同时**扩大了联合状态空间的覆盖范围**。
- 在低数据 regime 下（如 Fetch-Push 只用 4K 数据），CAIAC 也能明显提升性能，而其他方法甚至损害性能。
- **基于 Transformer 的启发式方法（CoDA、CoDA-action）在因果影响检测上不准确**，生成的样本大多不可行，导致性能下降。
- **CAIAC 可作为独立模块与任何离线学习算法结合**，无需环境交互。

## 7. 优点
- **理论驱动**：基于互信息和局部因果图，具有坚实的因果理论基础。
- **实用性强**：仅需离线数据即可生成反事实样本，无需环境交互或模型 rollout，避免了复合误差。
- **模块化**：独立于下游学习算法，易于集成到现有离线 RL 或技能学习框架中。
- **有效解决因果混淆**：通过显式识别动作无关实体并交换，直接打破伪相关。
- **实验设计充分**：不仅比较最终性能，还验证了生成样本的可行性和支持覆盖，并对阈值进行了系统分析。

## 8. 不足与局限
- **强假设**：假设实体间相互作用稀疏甚至不存在。在高度交互的环境（如物体碰撞、推搡）中，该假设可能不成立，导致生成不合法样本。论文也承认这是主要局限。
- **只关注动作影响，忽略对象间因果关系**：即使动作对实体无影响，实体之间也可能存在因果关系（例如一个物体移动导致另一个被动移动），但这些被忽略。
- **阈值依赖**：需要调优阈值 $\theta$，论文使用了网格搜索，但实际应用中可能较难设定。
- **对某些任务全覆盖困难**：在 Franka-Kitchen 的完整实验中，某些任务（hinge cabinet）所有方法几乎都失败，说明仅靠数据增强可能不足以解决根本性的演示不足问题（缺少从初始状态出发的成功轨迹）。
- **计算开销**：虽然 CAIAC 生成 cost 较低，但需要额外训练一个状态条件的转移模型，且每生成一个样本需要多次前向传播（K=64 个动作样本）。
- **低数据下联合模型训练可能存在风险**：当 CAIAC+MBPO 结合时，若部分生成样本不可行，可能污染动力学模型导致更差性能。

（完）
