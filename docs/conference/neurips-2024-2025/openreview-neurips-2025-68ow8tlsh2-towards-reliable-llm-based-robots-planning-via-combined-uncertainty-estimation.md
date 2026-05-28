---
title: Towards Reliable LLM-based Robots Planning via Combined Uncertainty Estimation
title_zh: 通过组合不确定性估计实现可靠的基于LLM的机器人规划
authors: "Shiyuan Yin, Chenjia Bai, Zhang Zihao, Junwei Jin, Xinxin Zhang, Chi Zhang, Xuelong Li"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=68OW8tLSh2"
tags: ["query:ur"]
score: 4.0
evidence: 面向可靠机器人规划的LLM不确定性估计
tldr: 大语言模型（LLM）在机器人规划中可能出现幻觉，导致不安全计划。现有不确定性估计方法未能区分认知不确定性和固有不确定性，影响有效性。本文提出CURE方法，将不确定性分解为认知和固有两部分，更精确地评估计划可靠性。在机器人规划任务中，CURE能够识别不可靠计划，提高实际执行的安全性。该方法有助于构建更可靠的机器人规划系统。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
motivation: LLM在机器人规划中的幻觉导致不安全计划，现有不确定性估计未充分区分不同类型。
method: 提出CURE方法，将不确定性分解为认知和固有不确定性，用于评估规划可靠性。
result: 在机器人规划任务中，CURE有效识别不可靠计划，提升安全性。
conclusion: CURE通过细粒度不确定性估计增强了LLM规划的可信度。
---

## Abstract
Large language models (LLMs) demonstrate advanced reasoning abilities, enabling robots to understand natural language instructions and generate high-level plans with appropriate grounding. However, LLM hallucinations present a significant challenge, often leading to overconfident yet potentially misaligned or unsafe plans. While researchers have explored uncertainty estimation to improve the reliability of LLM-based planning, existing studies have not sufficiently differentiated between epistemic and intrinsic uncertainty, limiting the effectiveness of uncertainty estimation.
In this paper, we present Combined Uncertainty estimation for Reliable Embodied planning (CURE), which decomposes the uncertainty into epistemic and intrinsic uncertainty, each estimated separately. Furthermore, epistemic uncertainty is subdivided into task clarity and task familiarity for more accurate evaluation. The overall uncertainty assessments are obtained using random network distillation and multi-layer perceptron regression heads driven by LLM features. 
We validated our approach in two distinct experimental settings: kitchen manipulation and tabletop rearrangement experiments. The results show that, compared to existing methods, our approach yields uncertainty estimates that are more closely aligned with the actual execution outcomes. The code is at https://github.com/Firesuiry/CURE.

---

## 论文详细总结（自动生成）

### 论文中文总结

#### 1. 论文的核心问题与整体含义（研究动机和背景）

大语言模型（LLM）在机器人任务规划中展现出强大的推理能力，能将自然语言指令转化为可执行的高层计划。但LLM存在“幻觉”问题，即过度自信地输出看似合理但实际上不可行或不安全的计划。现有不确定性估计方法未能细致区分**认知不确定性**（模型知识不足）和**固有不确定性**（环境随机性），导致估计不准确，难以有效识别不可靠计划。本研究旨在通过更精确的不确定性分解与估计，提升LLM规划在机器人任务中的可靠性。

#### 2. 论文提出的方法论：核心思想、关键技术细节

**核心思想**：提出 **CURE（Combined Uncertainty estimation for Reliable Embodied planning）** 框架，将规划不确定性分解为：
- **认知不确定性（Epistemic Uncertainty）**：进一步细分为**任务清晰度**（task clarity）和**任务熟悉度**（task familiarity）。
- **固有不确定性（Intrinsic Uncertainty）**：即预期任务成功率（expected success rate）。

**关键技术**：
1. **任务熟悉度评估**：使用**随机网络蒸馏（RND）**。固定目标网络，训练预测网络拟合其输出；对当前任务特征向量，预测误差越大表示任务越陌生，不确定性越高。
2. **任务清晰度评估**：提供两种方式
   - **慢速方法**：直接通过LLM查询（利用提示词判断指令是否模糊）。
   - **快速方法**：使用**不确定性评估网络（UAN）**，以LLM最后一层隐藏特征为输入，输出清晰度分数 `A_amb` 和预期成功率 `p`，联合训练。
3. **最终不确定性公式**：
   \[
   U = 1 - \alpha_1 \cdot (1 - \alpha_2 \cdot A_{\text{amb}}) \cdot p + \alpha_3 \cdot A_{\text{sim}}
   \]
   其中 \(A_{\text{sim}}\) 为RND输出的相似度度量（越大越不熟悉），\(\alpha_1,\alpha_2,\alpha_3\) 为可调超参数。

**算法流程**：给定自然语言指令 \(I\) 和环境观测 \(O\) → LLM 生成计划 \(A\) → 提取特征向量 \(T\) → 分别通过UAN和RND得到 \(p\)、\(A_{\text{amb}}\)、\(A_{\text{sim}}\) → 计算综合不确定性 \(U\) → 若 \(U\) 高则停止执行或请求人工帮助。

#### 3. 实验设计

- **场景与数据集**：
  - **厨房操作**（Mobile Manipulator in a Kitchen）：沿用 KnowNo 的任务设定。机器人需在厨房柜台前操作物体（如放入垃圾桶/抽屉），包含模糊指令和潜在不安全动作。
  - **桌面重排**（Tabletop Rearrangement）：在 PyBullet 仿真中，机器人需根据模糊指令移动彩色方块或碗。

- **Benchmark**：使用**SR-HR-AUC**（归一化帮助率-成功率曲线下面积）和**Spearman秩相关系数**（及p值）评估不确定性估计与任务成功率的相关性。

- **对比方法**：
  - 基线：KnowNo、IntroPlan、Vanilla、CoT、Self-probing、Self-probing-log、Top-k、Multi-step 等LLM不确定性估计方法。
  - 消融变体：Ambiguity、CURE w/o sim、KnowNo-Ambiguity、CURE、CURE-Ambiguity。

#### 4. 资源与算力

文中明确说明：
- 服务器配置：双路 Intel Xeon Gold 6348 处理器，512GB RAM，四张 NVIDIA A100-PCIE-40GB GPU。
- 单次实验耗时约 **12小时**。
- 厨房操作使用 Llama-3.3-70B-Instruct（规划器），桌面重排使用 Llama-3.2-8B-Instruct。

#### 5. 实验数量与充分性

- 主要报告了**两个场景**的实验结果（表1、表3），分别包含7-8种对比方法及多种消融变体。
- 在厨房场景中还进行了**CURE+IntroPlan 对比实验**（表2），评估过步率、过问率、帮助率。
- 附录中包含**超参数搜索实验**（图8：α2、α3的调优）、**数据集规模影响实验**（表4：从100到100k样本）、**校准实验**（目标成功率85%时实际达84.33%）。
- **充分性评价**：实验场景覆盖移动操作和桌面操作，对比了多种主流方法，进行了消融和超参数分析，统计显著性通过p值报告，图4、6、7展示了置信区间。整体实验设计较充分、公平。

#### 6. 论文的主要结论与发现

- CURE在所有指标上全面超越基线方法：在厨房操作中CURE-Ambiguity的Spearman相关系数达0.466，SR-HR-AUC达0.547；桌面重排中CURE的Spearman达0.635，SR-HR-AUC达0.732。
- 分解认知不确定性（清晰度+熟悉度）能显著提升不确定性估计的准确性。
- RND模块有效捕捉任务熟悉度，UAN能快速估计清晰度和成功率。
- CURE可以与现有规划器（如KnowNo、IntroPlan）无缝集成，进一步提升安全性（降低过步率）。

#### 7. 优点

- **不确定性细粒度分解**：将认知不确定性进一步拆分为任务清晰度和熟悉度，更贴近认知科学原理，具有理论依据和实用价值。
- **方法即插即用**：CURE不依赖特定LLM规划器结构，可独立附加于任何规划流程。
- **提供两种清晰度评估方式**：慢速LLM查询（准确）和快速UAN网络（高效），可根据需求灵活选择。
- **实验指标新颖**：提出SR-HR-AUC，能公平消除基线成功率的干扰，更准确反映不确定性质量。
- **代码开源**：便于复现和后续研究。

#### 8. 不足与局限

- **需预训练**：UAN和RND网络需在特定任务集上预训练，缺乏跨任务泛化能力；新环境需要重新收集数据训练。
- **未校准**：当前不确定性输出未与实际成功率直接校准，需要额外标定步骤对齐置信度。
- **实验场景有限**：仅验证了厨房操作和桌面重排两种仿真场景，未涉及真实机器人或更复杂的长时域任务。
- **计算资源需求高**：LLM推理和RND训练仍需较高算力，实时性可能受限。
- **超参数依赖**：α1,α2,α3需要针对任务调整（论文在厨房场景下调优），迁移性有待验证。

（完）
