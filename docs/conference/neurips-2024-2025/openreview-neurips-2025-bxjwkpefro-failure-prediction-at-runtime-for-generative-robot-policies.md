---
title: Failure Prediction at Runtime for Generative Robot Policies
title_zh: 生成式机器人策略的运行时故障预测
authors: "Ralf Römer, Adrian Kobras, Luca Worbis, Angela P. Schoellig"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=BXJWKpEfro"
tags: ["query:ur"]
score: 9.0
evidence: 生成式机器人策略的运行时故障预测
tldr: 该论文提出FIPER框架，用于生成式模仿学习策略的运行时早期故障预测。FIPER无需故障数据，通过随机网络蒸馏检测策略嵌入空间中的分布外观测，并结合高不确定性指标预判失败。实验证明该方法能有效识别即将发生的任务失败，为人形机器人等安全关键应用提供保障。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-bxjwkpefro/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1457, \"height\": 455, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-bxjwkpefro/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 931, \"height\": 277, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-bxjwkpefro/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1444, \"height\": 358, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-bxjwkpefro/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1414, \"height\": 495, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-bxjwkpefro/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1432, \"height\": 439, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-bxjwkpefro/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1423, \"height\": 444, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-bxjwkpefro/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 968, \"height\": 527, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-bxjwkpefro/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1452, \"height\": 526, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-bxjwkpefro/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1445, \"height\": 1070, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-bxjwkpefro/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1444, \"height\": 1298, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-bxjwkpefro/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1443, \"height\": 1296, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-bxjwkpefro/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1444, \"height\": 1297, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-bxjwkpefro/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1457, \"height\": 752, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-bxjwkpefro/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1125, \"height\": 301, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-bxjwkpefro/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 555, \"height\": 396, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-bxjwkpefro/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1413, \"height\": 567, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-bxjwkpefro/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1379, \"height\": 502, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-bxjwkpefro/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1406, \"height\": 1207, \"label\": \"Table\"}]"
motivation: 生成式策略在分布偏移下可能表现不可预测，需要运行时失败预警。
method: 提出FIPER，通过随机网络蒸馏检测分布外观测，并估计动作不确定性来识别失败前兆。
result: 在多个机器人任务上成功预测失败，无需失败样本。
conclusion: FIPER为部署安全关键机器人系统提供了有效的运行时故障检测手段。
---

## Abstract
Imitation learning (IL) with generative models, such as diffusion and flow matching, has enabled robots to perform complex, long-horizon tasks. However, distribution shifts from unseen environments or compounding action errors can still cause unpredictable and unsafe behavior, leading to task failure. Therefore, early failure prediction during runtime is essential for deploying robots in human-centered and safety-critical environments. We propose FIPER, a general framework for Failure Prediction at Runtime for generative IL policies that does not require failure data. FIPER identifies two key indicators of impending failure: (i) out-of-distribution (OOD) observations detected via random network distillation in the policy’s embedding space, and (ii) high uncertainty in generated actions measured by a novel action-chunk entropy score. Both failure prediction scores are calibrated using a small set of successful rollouts via conformal prediction. A failure alarm is triggered when both indicators, aggregated over short time windows, exceed their thresholds. We evaluate FIPER across five simulation and real-world environments involving diverse failure modes. Our results demonstrate that FIPER better distinguishes actual failures from benign OOD situations and predicts failures more accurately and earlier than existing methods. We thus consider this work an important step towards more interpretable and safer generative robot policies. Code, data, and videos are available at [tum-lsy.github.io/fiper_website](https://tum-lsy.github.io/fiper_website).

---

## 论文详细总结（自动生成）

# 论文《Failure Prediction at Runtime for Generative Robot Policies》中文总结

## 1. 核心问题与整体含义（研究动机和背景）

生成式模仿学习（IL）策略（如扩散模型、流匹配）使机器人能够执行复杂、长时域的任务。然而，在部署时，由于环境分布偏移（unseen distribution shifts）或动作预测的累积误差，策略可能表现出不可预测甚至危险的行为，导致任务失败。在以人为本、安全关键的场景中，关键需求是**在运行时早期预测失败**，以便及时干预或执行安全回退。

- 现有方法存在明显局限：纯分布外（OOD）检测器会在任何新场景触发警报，即使策略能泛化；基于视觉-语言模型（VLM）的方法只能在错误显现后报警，缺乏预见性；一些方法依赖于故障数据（failure data），这在真实场景中往往不可获得。
- 作者提出**FIPER（Failure Prediction at Runtime）**，一个通用的运行时故障预测框架，**不依赖任何故障数据**，仅需少量成功轨迹即可校准。核心思路是同时监控观测和动作两个维度的异常信号，结合逻辑与门（AND）触发故障警报。

## 2. 方法论：核心思想、关键技术细节

### 核心思想
FIPER 认为实际故障与两个指标同时出现相关：
1. **连续的分布外观测（OOD observations）**：观测在策略的嵌入空间中偏离成功轨迹的模式。
2. **生成动作中持续的高不确定性**：策略在给定观测下产生的动作分布具有高熵。

### 关键技术细节

#### 2.1 观测基分数：随机网络蒸馏（RND-OE）
- 采用随机网络蒸馏（Random Network Distillation, RND）在**策略的观测编码器嵌入空间**中检测OOD。
- 包含一个随机初始化的目标网络 `g(·)`（冻结）和一个预测网络 `f_θ(·)`。预测网络在成功轨迹数据 `D_ID` 上训练，使其输出拟合目标网络输出。
- **分数**：`s_RND(O_t) = ||f_θ(O_t) - g(O_t)||²`。观测偏离训练分布时，分数增大。
- 将分数在滑动窗口 `w_O` 内**累积求和**，得到 `η_O(τ:t)`。超过阈值 `γ_O,t` 则触发观测基警报。

#### 2.2 动作基分数：动作块熵（ACE）
- 从策略中采样一个批次（batch）动作块 `A_t`（`B` 个样本），计算每个预测时间步的**动作熵**，然后对所有步求和。
- **熵估计**：对每个动作维度进行分箱（binning），构建直方图计算概率。
- **分数**：`s_ACE(A_t) = Σ_i· ˆE( a^{(1)}_{t+i|t}, …, a^{(B)}_{t+i|t} )`。
- 同样在滑动窗口 `w_A` 内累积，得到 `η_A(τ:t)`。

#### 2.3 结合与校准（Conformal Prediction）
- **逻辑与（AND）**：FIPER 最终报警条件为 `F(τ:t) = 1` 当且仅当 `η_O(τ:t) > γ_{O,t}` 且 `η_A(τ:t) > γ_{A,t}`。
- **时间变化阈值**：使用 **一致性预测（Conformal Prediction）** 在少量成功轨迹（`M` 条）上校准阈值。分别计算每个时间步的均值 `μ_t` 和带宽 `b_t(δ)`，设置 `γ_t = μ_t + b_t`。文中比较了三种阈值类型：CP band、CP constant、time-varying。
- **理论保证**：对于新的成功轨迹（ID），误报概率的上界为 `δ`（Proposition 1）。

## 3. 实验设计

### 环境与数据集
- **三个仿真环境**：Sorting（推块入盒）、Stacking（堆叠方块）、PushT（推T形物体至目标位姿）。OOD通过改变物体尺寸、目标位置等方式引入。
- **两个真实世界任务**：Pretzel（折叠绳子成蝴蝶结形状）、Push Chair（移动机械臂推椅子至目标位置）。OOD包括绳索初始旋转、椅子初始位姿变化等。
- 策略：Sorting/Stacking 使用流匹配+Transformer（ACT架构）；PushT/Pretzel/PushChair 使用扩散+U-Net（Diffusion Policy架构）。图像编码器为ResNet-18。

### 基准方法
- **PCA-kmeans**：观测嵌入的PCA+聚类，距离衡量OOD。
- **logpZO**：流匹配学习观测嵌入分布，反向ODE得到噪声分数。
- **STAC**：相邻时间步动作块分布的MMD差异。
- **RND-A**：RND在动作块上学习置信度。

### 评估指标
- **平衡准确率 (Balanced Accuracy)** = (TPR + TNR)/2
- **归一化检测时间 (DT)** = 检测时间/最大回合长度
- **时间步加权准确率 (TWA)**：对正确预测的故障，奖励早期检测（1 - DT）
- 统计均值和标准差（5个随机种子），结果在九个分位数（0.9~0.99）上平均。

## 4. 资源与算力

论文在附录 B.6 中说明：
- **GPU**：单块 NVIDIA GeForce RTX 4090
- **CPU**：Intel Core i9-285K
- **内存**：64 GB RAM
- **运行时间**：评估所有方法、窗口大小和分位数，每种子约需 1 小时。
- **训练/推理开销**：RND-OE 需要额外训练（约250个epoch），但推理时计算量很小。ACE 需要采样一个批次动作块（Batch size B 为 30-256 不等）并计算直方图熵，在实验环境中可实时运行。文中指出对于极高维动作空间（如人形机器人）可能增加计算负担。

## 5. 实验数量与充分性

- **实验数量**：
  - 5 个环境 × 5 种子 × 9 分位数 × 多种窗口大小（1-50） = 大量组合。
  - 消融实验：窗口大小、阈值类型（CP band/constant/time-varying）、逻辑组合（AND vs OR）。
  - 单分数 vs. 联合分数（RND-OE、ACE、FIPER）对比。
- **充分性**：实验覆盖了不同机器人形态（Franka、移动机械臂）、不同生成模型（扩散、流匹配）、不同任务类型（推、堆叠、折叠、推送）。消融实验系统，对比方法全面，统计指标合理。
- **公平性**：所有方法使用相同成功轨迹数据 `D_ID` 进行训练/校准；超参数（窗口大小、阈值类型）按全体任务上最高 TWA 选取，避免对特定任务的偏袒。报告了均值与标准差。

## 6. 主要结论与发现

1. **FIPER 在平衡准确率和早期检测方面优于所有基线**：平均 TWA 0.65（最高），平衡准确率 0.78，仅次优的 logpZO 为 0.69。FIPER 的 TPR 平均 0.92，TNR 平均 0.65。
2. **观测基与动作基分数的结合（AND操作）比单独使用更鲁棒**：AND 操作大幅降低误报（TNR 提高），同时保持高 TPR（0.92）。
3. **滑动窗口累积优于单步或全累积**：单步（w=1）导致大量误报；全累积（STAC 风格）延迟检测，本质上是因失败轨迹更长而累积更高分数，而非早期预测。
4. **RND-OE 分数能更好区分成功 OOD 与失败 ID**：图4显示RND-OE在Success OOD与Fail ID之间有更大间隔，优于PCA-kmeans和logpZO。
5. **ACE 分数在动作多模态环境下优于 STAC**：STAC 在多模态任务（如 Sorting、Stacking）中 TPR 很低（<0.5），而 ACE 可达 0.76-0.99。
6. **阈值类型选择影响性能**：time-varying 阈值在 FIPER 上获得最佳 TWA；CP band/constant 提供理论保证的误报上界，但检测更晚。

## 7. 优点

- **无需故障数据**：仅需少量成功轨迹即可训练和校准，大大降低数据收集门槛。
- **通用性**：与具体生成模型（扩散/流匹配）、策略架构（U-Net/Transformer）、任务类型无关。
- **可解释性**：同时从观测和动作两个角度提供故障指示，有助于理解故障原因。
- **理论保证**：通过一致性预测给出误报率的概率上界（Proposition 1）。
- **评估新颖**：提出 TWA 指标，同时衡量准确率和早期性，更贴近实际需求。
- **实验广泛**：覆盖仿真和真实世界、多种故障模式，消融实验全面。
- **计算开销低**：RND-OE 和 ACE 在实验中可实时运行（使用单块RTX 4090）。

## 8. 不足与局限

- **仍需少量成功轨迹**：虽然无需故障数据，但需要收集若干成功的策略执行轨迹（仿真50条，真实10条），这在完全离线场景中可能仍有困难。
- **RND-OE 需要额外训练**：需训练与策略独立的 RND 模型，增加了离线阶段的成本。
- **时间变化阈值依赖时序规律**：如果成功轨迹在时序上高度差异（例如抓取顺序或时间长短不同），时间变化阈值可能不合理；此时常量阈值更合适。
- **未考虑更高维动作空间**：ACE 计算在笛卡尔空间中的末端执行器位置，但若动作维度极高（如人形机器人全身动作），计算量可能增大，文中未测试。
- **仅测试图像观测**：虽然预期能扩展到语言、触觉等模态，但未做实证。
- **历史信息利用有限**：仅通过滑动窗口累积分数，未将历史观测/动作直接用于计算不确定性。
- **存在误报和漏报**：平均平衡准确率 0.78，在某些任务（如 PushT）TNR 仅 0.44，仍有改进空间。

（完）
