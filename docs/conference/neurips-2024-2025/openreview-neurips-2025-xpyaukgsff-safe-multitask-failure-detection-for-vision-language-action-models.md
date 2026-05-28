---
title: "SAFE: Multitask Failure Detection for Vision-Language-Action Models"
title_zh: "SAFE: 面向视觉-语言-动作模型的多任务故障检测"
authors: "Qiao Gu, Yuanliang Ju, Shengxiang Sun, Igor Gilitschenski, Haruki Nishimura, Masha Itkina, Florian Shkurti"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=XPyAukgsFf"
tags: ["query:ur"]
score: 9.0
evidence: 针对机器人策略的多任务故障检测
tldr: 针对通用机器人策略（如视觉-语言-动作模型）在未见任务和环境中的故障检测问题，本文提出SAFE多任务故障检测器。通过分析模型内部状态与任务特征，SAFE能够在机器人执行新任务时及时预警失败，显著提升部署安全性。实验证明其在多种操作任务上泛化良好，为人形机器人等自主系统的可靠运行提供了关键支持。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1444, \"height\": 827, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1439, \"height\": 563, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1440, \"height\": 822, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1426, \"height\": 666, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1416, \"height\": 492, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1450, \"height\": 442, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1009, \"height\": 417, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1004, \"height\": 419, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1010, \"height\": 418, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1012, \"height\": 415, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1009, \"height\": 415, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 631, \"height\": 664, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 627, \"height\": 609, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 629, \"height\": 601, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 629, \"height\": 663, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 628, \"height\": 611, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 626, \"height\": 601, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1425, \"height\": 1923, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xpyaukgsff/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1406, \"height\": 1830, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-xpyaukgsff/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1456, \"height\": 663, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xpyaukgsff/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1454, \"height\": 358, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xpyaukgsff/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1243, \"height\": 593, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xpyaukgsff/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 623, \"height\": 386, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xpyaukgsff/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1453, \"height\": 324, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xpyaukgsff/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1172, \"height\": 393, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xpyaukgsff/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 848, \"height\": 315, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xpyaukgsff/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1454, \"height\": 575, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xpyaukgsff/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 654, \"height\": 922, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xpyaukgsff/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 736, \"height\": 1199, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xpyaukgsff/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1463, \"height\": 1074, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xpyaukgsff/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 680, \"height\": 549, \"label\": \"Table\"}]"
motivation: 现有故障检测器仅针对特定任务训练，无法泛化到通用机器人策略的新任务，导致部署风险。
method: 提出SAFE框架，基于VLA内部表征和任务嵌入，学习一个跨任务共享的失败分类器，实现多任务故障检测。
result: 在多个未见任务上，SAFE相比基线方法显著提高了故障检测的准确率和召回率。
conclusion: SAFE提供了一种可扩展的故障检测方案，使通用机器人策略能在未知环境中安全运行。
---

## Abstract
While vision-language-action models (VLAs) have shown promising robotic behaviors across a diverse set of manipulation tasks, they achieve limited success rates when deployed on novel tasks out of the box. To allow these policies to safely interact with their environments, we need a failure detector that gives a timely alert such that the robot can stop, backtrack, or ask for help. However, existing failure detectors are trained and tested only on one or a few specific tasks, while generalist VLAs require the detector to generalize and detect failures also in unseen tasks and novel environments. In this paper, we introduce the multitask failure detection problem and propose SAFE, a failure detector for generalist robot policies such as VLAs. We analyze the VLA feature space and find that VLAs have sufficient high-level knowledge about task success and failure, which is generic across different tasks. Based on this insight, we design SAFE to learn from VLA internal features and predict a single scalar indicating the likelihood of task failure. SAFE is trained on both successful and failed rollouts and is evaluated on unseen tasks. SAFE is compatible with different policy architectures. We test it on OpenVLA, $\pi_0$, and $\pi_0$-FAST in both simulated and real-world environments extensively. We compare SAFE with diverse baselines and show that SAFE achieves state-of-the-art failure detection performance and the best trade-off between accuracy and detection time using conformal prediction. More qualitative results and code can be found at the project webpage: https://vla-safe.github.io/

---

## 论文详细总结（自动生成）

# 论文《SAFE: Multitask Failure Detection for Vision-Language-Action Models》中文总结

## 1. 核心问题与整体含义（研究动机与背景）

- **问题**：视觉-语言-动作模型（VLA）作为通用机器人策略，在未见过的任务和环境中成功率较低（30-60%），需要及时检测失败以保障安全交互。
- **现有局限**：传统故障检测方法只针对单一任务训练和测试，无法泛化到新任务；一些任务通用检测器要么需要多次采样动作（高开销），要么需要查询大型VLM（实时性差）。
- **本文目标**：提出首个面向通用VLA的**多任务故障检测**问题，设计一个能在**零样本**情况下泛化到未见任务的、高效实时的故障检测器。

## 2. 方法论：核心思想、关键技术细节

- **核心思想**：分析VLA内部特征空间，发现成功与失败的 rollouts 在特征空间中分离，且这种分离在不同任务间保持一致（存在“失败区域”）。因此可以从VLA内部特征中学习通用失败表征。
- **SAFE 框架**：
  1. **特征提取**：从VLA的最后一层（解码为token logits或速度场之前）提取隐状态向量，经过聚合（如取第一个、最后一个、均值、首尾拼接）得到固定维度的嵌入向量 \( e_t \)。
  2. **失败分数预测器**：
     - **SAFE-MLP**：对每个时间步独立地用MLP \( g(\cdot) \) 将 \( e_t \) 映射为标量，再通过sigmoid取累积和作为失败分数 \( f_{\text{MLP}}(e_{0:t}) = \sum_{\tau=1}^t \sigma(g(e_\tau)) \)。训练使用L1损失。
     - **SAFE-LSTM**：用LSTM顺序处理特征流，输出经sigmoid归一化的分数 \( s_t \in [0,1] \)。训练使用二值交叉熵损失。
     - 两者均简单（1-2层），避免过拟合，提升泛化。
  3. **阈值选择**：采用**函数化共形预测（Functional Conformal Prediction, CP）** ，在成功rollouts校准集上构建时变预测带 \( C_\alpha \)，保证新成功rollout的分数以概率 \( 1-\alpha \) 落在带内；超出的时间点即检测为失败。

## 3. 实验设计：数据集、Benchmark 与对比方法

- **仿真平台**：
  - **LIBERO-10**：10个长时任务，涵盖多种物体、布局和指令。测试模型：OpenVLA、\( \pi_0 \)、\( \pi_0 \)-FAST。
  - **SimplerEnv**：高保真仿真，复现RT系列和BridgeData V2环境。测试模型：\( \pi_0^* \)（复现版），分Google Robot和WidowX两种 embodiment。
- **真实机器人**：
  - **Franka Emika Panda**：用 \( \pi_0 \)-FAST-DROID checkpoint，设计13个任务，每任务30成功/30失败。
  - **WidowX 250**：用OpenVLA预训练模型，收集8个任务共532个rollouts（244成功/288失败）。
- **评估协议**：
  - 将任务分为Seen（训练+校准）和Unseen（测试泛化），按不同随机种子划分。
  - 指标：ROC-AUC（基于最大分数）、平衡准确率（Bal-acc）、平均检测时间（T-det）以及CP框架下的TPR、FPR。
- **对比基线**（三大类）：
  1. **Token不确定性**（单次推理）：最大/平均概率、最大/平均熵。
  2. **样本一致性**（需多次采样）：动作总变差、翻译/旋转/夹爪变差、聚类熵。
  3. **特征距离**（基于VLA嵌入）：马氏距离、k-NN（欧氏/余弦）、PCA-KMeans、RND、LogpZO、STAC（及STAC-Single）。

## 4. 资源与算力

- **明确说明**：
  - 训练和评估在单张 **NVIDIA A100 40GB GPU** 上完成。
  - SAFE模型（MLP/LSTM）仅1-2层，训练时间通常**不到1分钟**。
  - 推理时SAFE的额外开销**<1ms**（小于VLA推理时间的1%）。
- **未说明**：VLA模型本身的训练算力（论文使用作者已发布的微调检查点，未训练VLA）。

## 5. 实验数量与充分性

- **总实验量**：涵盖3个仿真Benchmark（LIBERO-10、SimplerEnv两个embodiment）和2个真实机器人平台，共5个评估场景。
- **多次重复**：仿真结果平均 **3个随机种子**（不同Seen/Unseen任务划分），真实实验平均 **5个随机种子**。每个种子下任务划分不同，保证了泛化评估的稳健性。
- **消融实验**：
  - 特征聚合方式（First/Last/Mean/First&Last）的对比。
  - 不同训练任务数量（1,3,5,7）的影响。
  - 与通用视觉特征（DINOv2、CLIP）的比较。
- **公平性**：与16种以上基线方法对比，包括最新的FAIL-Detect（LogpZO）和STAC。所有基线调优到最佳超参数。
- **充分性**：实验设计覆盖了从仿真到真实、从多任务到零样本泛化、从准确率到时延的多维度评估，结果丰富且客观。

## 6. 主要结论与发现

- **VLA内部特征对任务成功/失败具有可分离性**：t-SNE可视化显示不同任务间的失败特征聚集在同一区域（“失败区域”），成功特征远离该区域。
- **SAFE在所有评估设置中达到最优或近最优**：
  - 仿真平均ROC-AUC：SAFE-MLP在Seen任务81.43%，Unseen任务78.00%；SAFE-LSTM在Unseen任务77.04%。相比最佳基线（余弦k-NN, 73.93%）提升约4-5%。
  - 真实Franka实验：SAFE-MLP在Unseen任务达到64.16%（高于最佳基线Mahalanobis 53.93%）；真实WidowX实验：SAFE-MLP在Unseen任务88.42%（最佳基线马氏距离70.00%）。
- **CP框架下SAFE取得最佳准确率-检测时间权衡**：能在早期（甚至失败发生前）高置信度检测失败。
- **SAFE推理效率高**：额外计算极低，适合实时部署。

## 7. 优点

- **问题新颖且实用**：首次系统定义多任务故障检测问题，针对通用VLA策略的实际部署需求。
- **方法简洁高效**：仅利用VLA最后一层特征+轻量级MLP/LSTM，无需额外采样或大模型查询，训练快、推理快。
- **强泛化能力**：在零样本未见任务上表现优异，优于多种基于OOD或不确定性量化的基线。
- **理论保障**：通过共形预测提供时变阈值，可调节误报率。
- **实验全面**：覆盖多种VLA架构（OpenVLA, π0, π0-FAST）、多种embodiment、仿真与真实环境，基线丰富，消融充分。

## 8. 不足与局限

- **仅限操作任务**：未验证是否可泛化到其他embodiment（如人形机器人）、sim-to-real迁移或动作缺失的视频数据。
- **依赖VLA内部特征**：需要白盒访问VLA的最后一层嵌入；黑盒VLA（不提供特征）无法直接适用。
- **训练仍需失败数据**：尽管无需为新任务单独收集，但仍需在若干Seen任务上收集成功与失败rollouts（数百条）。对于全新任务类别，若失败模式与训练任务差异极大，泛化可能下降。
- **特征聚合方式有限**：仅使用最后一层特征；未探索多层特征融合或中间层特征，可能错过更丰富信息。
- **CP假设可能不满足**：共形预测的交换性假设在跨任务泛化时不一定成立，导致TNR偏离理论保证（论文已观察到该现象）。
- **实时性仅定性说明**：虽声称额外开销<1ms，但未在真实机器人控制循环中系统测量端到端延迟。

（完）
