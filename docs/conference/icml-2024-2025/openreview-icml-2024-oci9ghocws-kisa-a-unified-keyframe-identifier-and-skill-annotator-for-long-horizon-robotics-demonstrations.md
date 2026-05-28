---
title: "KISA: A Unified Keyframe Identifier and Skill Annotator for Long-Horizon Robotics Demonstrations"
title_zh: "KISA: 面向长程机器人演示的统一关键帧识别与技能标注器"
authors: "Longxin Kou, Fei Ni, YAN ZHENG, Jinyi Liu, Yifu Yuan, Zibin Dong, Jianye HAO"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=oCI9gHocws"
tags: ["query:ur"]
score: 7.0
evidence: 机器人演示的关键帧识别与技能标注
tldr: 本文提出KISA，利用预训练的视觉-语言表示，自动从长程机器人演示中识别关键帧并标注技能，解决了现有方法精度低且缺乏语义关联的问题。该方法为构建高质量机器人操作数据集提供了高效工具，在多个任务上验证了有效性。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 855, \"height\": 518, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1663, \"height\": 894, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 834, \"height\": 523, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 848, \"height\": 360, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 823, \"height\": 398, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 843, \"height\": 324, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 847, \"height\": 296, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 847, \"height\": 358, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1742, \"height\": 1143, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1727, \"height\": 825, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1418, \"height\": 737, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 928, \"height\": 815, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1291, \"height\": 823, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1291, \"height\": 823, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1297, \"height\": 826, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1294, \"height\": 809, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1287, \"height\": 770, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1289, \"height\": 766, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1284, \"height\": 770, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1290, \"height\": 764, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1293, \"height\": 760, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1294, \"height\": 760, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1297, \"height\": 761, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1294, \"height\": 758, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1247, \"height\": 1608, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1081, \"height\": 816, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-oci9ghocws/fig-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 1086, \"height\": 723, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-oci9ghocws/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1768, \"height\": 376, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-oci9ghocws/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 856, \"height\": 238, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-oci9ghocws/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 894, \"height\": 453, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-oci9ghocws/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 859, \"height\": 303, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-oci9ghocws/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 851, \"height\": 296, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-oci9ghocws/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1186, \"height\": 387, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-oci9ghocws/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 860, \"height\": 344, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-oci9ghocws/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 878, \"height\": 388, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-oci9ghocws/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 692, \"height\": 367, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-oci9ghocws/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 683, \"height\": 626, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-oci9ghocws/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1720, \"height\": 499, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-oci9ghocws/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1411, \"height\": 346, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-oci9ghocws/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1414, \"height\": 332, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-oci9ghocws/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1522, \"height\": 1448, \"label\": \"Table\"}]"
motivation: 从长程演示中学习策略需要关键帧引导和技能标注，但现有方法精度和语义不足。
method: 提出统一的KISA框架，使用预训练视觉-语言模型实现时序增强的关键帧识别与技能标注。
result: 在跨任务演示分解上优于基线，提供可解释的关键帧和语义标注。
conclusion: KISA能高效构建机器人演示数据集，支持后续策略学习。
---

## Abstract
Robotic manipulation tasks often span over long horizons and encapsulate multiple subtasks with different skills. Learning policies directly from long-horizon demonstrations is challenging without intermediate keyframes guidance and corresponding skill annotations. Existing approaches for keyframe identification often struggle to offer reliable decomposition for low accuracy and fail to provide semantic relevance between keyframes and skills. For this, we propose a unified **K**eyframe **I**dentifier and **S**kill **A**notator (**KISA**) that utilizes pretrained visual-language representations for precise and interpretable decomposition of unlabeled demonstrations. Specifically, we develop a simple yet effective temporal enhancement module that enriches frame-level representations with expanded receptive fields to capture semantic dynamics at the video level. We further propose coarse contrastive learning and fine-grained monotonic encouragement to enhance the alignment between visual representations from keyframes and language representations from skills. The experimental results across three benchmarks demonstrate that KISA outperforms competitive baselines in terms of accuracy and interpretability of keyframe identification. Moreover, KISA exhibits robust generalization capabilities and the flexibility to incorporate various pretrained representations.

---

## 论文详细总结（自动生成）

# 论文 KISA 详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **问题**：机器人操作任务常涉及长时间跨度（long-horizon）和多个子任务，需要关键帧（keyframe）和技能标注来指导策略学习。然而，现有无标注演示中自动识别关键帧的方法精度低，且缺乏语义可解释性（关键帧与技能之间无明确关联）。
- **背景**：直接端到端学习长时域演示容易出现复合误差；层次化策略学习需要明确的子任务边界和技能标注，但获取这些标注成本高昂。现有方法如 VideoRLCS 依赖奖励或动作等特权信息，局限性强；UVD 等启发式方法基于预训练视觉特征，但缺少语言引导，易误检。
- **动机**：利用预训练的视觉‑语言表示（如 R3M、VIP、LIV）自动、可扩展、语义有意义地从无标签视频演示中识别关键帧并标注技能。

## 2. 论文提出的方法论：核心思想、关键技术细节、算法流程
- **核心思想**：构建统一的 **KISA**（Keyframe Identifier and Skill Annotator）框架，通过时序增强将静态帧级特征扩展为视频级表示，再与语言技能表示对齐，使得关键帧处的置信度分数出现明显峰值，从而实现精确且可解释的分解。
- **关键技术细节**：
  - **时序增强模块（Temporal Enhancement Module）**：基于多层 Transformer Encoder，将当前帧及历史帧的预训练视觉特征（来自 R3M、VIP 或 LIV）聚合，加入位置编码，使每个帧的表示能捕获长程语义动态，弥合静态图像与视频之间的差距。
  - **历史感知对比学习（History‑aware Contrastive Learning）**：在帧‑技能对齐训练中，除了标准错误技能负样本外，还构造两种更难负样本：
    1. 不匹配历史帧 + 正确技能（防止过拟合孤立帧）；
    2. 视频时序反转 + 正确技能（语义反转）。
    损失函数：`L_contrastive = L_video + L_history + L_reverse`，均基于 InfoNCE。
  - **细粒度单调对齐（Fine‑grained Monotonic Alignment）**：为防止同技能内帧表示坍塌，引入分数距离损失 L_score，鼓励每个子技能片段内，帧与对应技能的相似度随时间单调递增，且与该帧到子技能末端关键帧的视觉距离分数保持一致。总损失：`L_total = L_contrastive + α·L_score`。
- **算法流程**（文字描述）：
  1. 对每个输入帧 o_i 及其历史帧 h_i，通过预训练图像编码器 φ 提取帧特征，再经时序增强模块 Φ 得到视频级表示 v_i = Φ(h_i, o_i)。
  2. 计算 v_i 与技能库中所有技能语言表示 ℓ_s 的余弦相似度，取最大值为该帧的置信度分数 f_i = max cos(v_i, ℓ_s)。
  3. 训练时使用对比损失和单调对齐损失联合优化 Φ 和语言编码器（图像编码器可冻结或微调）。
  4. 推理时，在整段视频的置信度分数序列中检测局部峰值，峰值对应的帧即为关键帧，其对应的技能为置信度最高的技能。

## 3. 实验设计：数据集 / 场景、Benchmark、对比方法
- **数据集 / 场景**：
  - **Maniskill2**：20+ 种操作任务，含刚性/软体物体，提供 80k 演示轨迹，使用特权信息标注真实关键帧和技能。
  - **CALVIN**：语言引导的长时域操作，Franka 机器人，25k 演示轨迹，任务链长度 2‑10 个子任务。
  - **FrankaKitchen**：厨房场景，7 个子任务（微波炉、水壶、灯开关、柜子等），共 12k 演示，每段演示含 4 个随机顺序子任务。
- **对比方法**：
  - 无监督方法：KTS（核时间分割）
  - 奖励驱动：VideoRLCS
  - 预训练表示直接使用：R3M、VIP、LIV（并分别用两种方式评估视觉距离和视觉‑语言相似度）
  - 启发式方法：UVD（基于 LIV 视觉特征）
  - 微调基线：FT‑R3M、FT‑VIP、FT‑LIV（用标准对比学习进行帧级对齐）
- **评估指标**：
  - 关键帧：数量误差、MAE（时间偏差）、F1‑score
  - 技能：Top‑1 准确率

## 4. 资源与算力
- **硬件**：论文附录提到在 **Intel(R) Xeon(R) Gold 6226R CPU @ 2.90GHz** 和 **NVIDIA A800 PCIe 80 GB** 单卡上训练。未明确说明 GPU 数量（可能为单卡）。
- **训练时长**：
  - Maniskill2：200 个 epoch × 80k 演示，约 200 小时。
  - CALVIN：300 epoch × 25k 演示，约 200 小时。
  - FrankaKitchen：200 epoch × 12k 演示，约 20 小时。
- **模型规模**：时序增强模块为 6 层 Transformer，隐藏维度 1024，8 头注意力。不同变体使用不同图像编码器（R3M、VIP、LIV），参数量有差异（文中未精确给出总参数量，但提到联合训练时模型大小从 169M 到 253M 不等）。

## 5. 实验数量与充分性
- **实验组数**：
  - **主实验**（表 1、图 4）：三个数据集上关键帧识别和技能标注的主要结果，报告 5 个不同种子的均值和方差。
  - **零样本泛化实验**（表 2、图 5）：三层难度（对象泛化 L1、组合泛化 L2、跨实体泛化 L3），共三个场景。
  - **消融实验**（表 3）：在三个表示骨架上依次移除时序增强、历史对比学习、单调对齐，报告 Top‑1 准确率下降情况。
  - **历史长度影响**（表 5）：固定窗口大小从 8 到 40 帧，以及使用当前技能段内历史与全部历史的对比。
  - **多域联合训练**（图 8）：合并三个数据集训练，比较不同模型大小（169M、211M、253M）的表现。
  - **策略学习有效性**（表 4）：在 CALVIN 上对比 LCBC、LISA、LISA+LIV、LISA+KISA 的成功率和平均任务长度。
  - **可视化分析**（图 7、图 9‑27）：热力图、t‑SNE 技能空间、示例分解展示。
- **充分性与公平性**：实验设计较为完整，覆盖多个数据集、多种基线（包括无监督、启发式、预训练直接使用和微调版本），并报告了多次运行的统计量。消融实验系统性验证了每个模块的作用。零样本泛化设置了三种难度，考虑了跨对象的颜色/形状/物体种类、技能组合、甚至跨实体（仿真→真实）的迁移。但跨实体泛化（L3）仅在 RealKitchen 上测试，且只使用 LIV 骨架子集（文中未给出完整结果方差较大）。整体而言，实验数量足够，对比公平。

## 6. 论文的主要结论与发现
1. **精度领先**：KISA 在所有三个数据集上的关键帧识别 F1‑score 均超过 85%（CALVIN）甚至接近 99%（Maniskill2、FrankaKitchen），显著优于所有基线（UVD 最高约 64%）。
2. **技能标注准确**：KISA 的 Top‑1 准确率在三个数据集上分别达 99.2%、94.7%、96.1%，相比 FT‑LIV（微调版）提升 20‑30 个百分点。
3. **强零样本泛化**：即使在未见的物体外观、任务组合甚至跨实体（仿真→真实）场景下，KISA 仍保持远高于基线的性能（F1‑score 从 40%→80%+/90%+）。
4. **促进策略学习**：使用 KISA 标注的关键帧和技能，可显著提升层次化策略（LISA）在长时域任务上的成功率和平均完成任务长度（从 2.2 提升到 2.7 个子任务）。
5. **历史帧至关重要**：时序增强模块是最大的贡献来源，移除后性能骤降；使用完整历史较固定窗口更优；历史范围限制在当前技能段内即可取得接近全历史的性能。

## 7. 优点：方法或实验设计上的亮点
- **方法亮点**：
  - **统一框架**：同时解决关键帧识别和技能标注两个问题，输出语义可解释的分解。
  - **即插即用**：时序增强模块可灵活接入任意预训练视觉表示（R3M、VIP、LIV），无需重新训练整个编码器。
  - **历史感知对比**：设计的三种负样本（错误技能、不匹配历史、时序反转）有效增强了对于动作语义的理解，避免过拟合静态帧。
  - **单调对齐**：简单有效的正则项，在不增加人工标注成本下促进技能内部分辨率，防止表示坍塌。
- **实验亮点**：
  - **三个不同风格的长时域基准**：覆盖通用操作（Maniskill2）、语言条件（CALVIN）、厨房操作（FrankaKitchen），增加结论普适性。
  - **系统性零样本泛化**：按对象、组合、实体三层递进评估，并给出可视化案例（图 25‑27）。
  - **模型规模扩展实验**：验证更大模型缓解域冲突，展示了向互联网规模扩展的潜力。
  - **与策略学习结合**：直接证明标注质量对下游任务的影响，具有实际应用价值。

## 8. 不足与局限
- **实验覆盖**：
  - 跨实体泛化 (L3) 仅在 RealKitchen 上测试，且只展示了一个例子，F1‑score 为 40.7%，方差较大（14.8%），说明从仿真到真实机器人演示仍有挑战，但文中未深入分析原因。
  - 策略学习实验仅基于 CALVIN，未在其他数据集验证标注对策略的增益。
  - 联合训练实验中域冲突现象未充分解决，仅指出加大模型可缓解，未探索域对齐技术。
- **方法局限**：
  - **技能标注为闭集检索**：当前技能来自固定技能库，不能进行开放词汇生成（如用多模态大模型生成本地描述）。作者承认此局限。
  - **依赖仿真数据微调**：KISA 的第一阶段完全基于仿真环境中带有真实关键帧标签的演示进行训练，对真实互联网视频的通用性尚未验证。
  - **历史帧范围限制**：虽然使用全部历史效果最好，但固定长窗口仍可取得不错性能，说明对历史长度有敏感性，实际应用中需根据子技能平均长度调参。
- **偏差风险**：文中使用的预训练表示（R3M、VIP、LIV）均基于 Ego4D 等特定数据集，可能存在对视角、物体类别、场景的隐式偏好，影响在下游操作任务上的泛化边界。

（完）
