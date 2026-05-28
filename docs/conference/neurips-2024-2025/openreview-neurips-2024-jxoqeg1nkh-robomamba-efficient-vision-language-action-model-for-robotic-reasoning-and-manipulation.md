---
title: "RoboMamba: Efficient Vision-Language-Action Model for Robotic Reasoning and Manipulation"
title_zh: RoboMamba：面向机器人推理和操作的高效视觉-语言-动作模型
authors: "Jiaming Liu, Mengzhen Liu, Zhenyu Wang, Pengju An, Xiaoqi Li, Kaichen Zhou, Senqiao Yang, Renrui Zhang, Yandong Guo, Shanghang Zhang"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=JxOQeg1NkH"
tags: ["query:ur"]
score: 4.0
evidence: 高效的视觉-语言-动作模型，线性推理复杂度，对边缘部署有潜在价值
tldr: 现有VLA模型计算成本高，难以部署于边缘。本文提出RoboMamba，基于Mamba状态空间模型构建端到端VLA模型，在保持推理和动作能力的同时实现线性推理复杂度，显著降低微调与推理开销，为机器人边缘部署提供了高效方案。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-jxoqeg1nkh/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1448, \"height\": 753, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jxoqeg1nkh/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1418, \"height\": 739, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jxoqeg1nkh/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1455, \"height\": 378, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jxoqeg1nkh/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1448, \"height\": 698, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jxoqeg1nkh/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1349, \"height\": 375, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jxoqeg1nkh/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1443, \"height\": 694, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jxoqeg1nkh/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 207, \"height\": 205, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-jxoqeg1nkh/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 631, \"height\": 767, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-jxoqeg1nkh/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1455, \"height\": 422, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-jxoqeg1nkh/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1263, \"height\": 261, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-jxoqeg1nkh/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 923, \"height\": 224, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-jxoqeg1nkh/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1447, \"height\": 310, \"label\": \"Table\"}]"
motivation: 现有VLA模型推理能力不足且计算成本高，限制部署。
method: 利用Mamba状态空间模型构建端到端VLA模型，实现线性推理复杂度。
result: 在多种操作任务上，RoboMamba以更低计算量达到或超越现有方法。
conclusion: Mamba架构在机器人VLA模型中兼顾效率与性能。
---

## Abstract
A fundamental objective in robot manipulation is to enable models to comprehend visual scenes and execute actions. Although existing Vision-Language-Action (VLA) models for robots can handle a range of basic tasks, they still face challenges in two areas: (1) insufficient reasoning ability to tackle complex tasks, and (2) high computational costs for VLA model fine-tuning and inference. The recently proposed state space model (SSM) known as Mamba demonstrates promising capabilities in non-trivial sequence modeling with linear inference complexity. Inspired by this, we introduce RoboMamba, an end-to-end robotic VLA model that leverages Mamba to deliver both robotic reasoning and action capabilities, while maintaining efficient fine-tuning and inference. Specifically, we first integrate the vision encoder with Mamba, aligning visual tokens with language embedding through co-training, empowering our model with visual common sense and robotic-related reasoning. To further equip RoboMamba with SE(3) pose prediction abilities, we explore an efficient fine-tuning strategy with a simple policy head. We find that once RoboMamba possesses sufficient reasoning capability, it can acquire manipulation skills with minimal fine-tuning parameters (0.1\% of the model) and time. In experiments, RoboMamba demonstrates outstanding reasoning capabilities on general and robotic evaluation benchmarks. Meanwhile, our model showcases impressive pose prediction results in both simulation and real-world experiments, achieving inference speeds 3 times faster than existing VLA models.

---

## 论文详细总结（自动生成）

好的，以下是根据您提供的论文内容生成的详细中文总结。

---

### 论文核心问题与整体含义（研究动机和背景）

- **背景**：大型语言模型（LLMs）和多模态大语言模型（MLLMs）在自然语言处理和视觉理解方面取得了显著进展，并在机器人操作领域得到应用。现有的视觉-语言-动作（VLA）模型（如OpenVLA、ManipLLM）能够处理基本任务，但面临两个主要挑战：
    1.  **推理能力不足**：在复杂的机器人推理任务（如长期任务规划、因果推断）上表现不佳。
    2.  **计算成本高昂**：基于Transformer的VLA模型在微调和推理时计算开销大，难以满足实时性要求。
- **动机**：近期提出的状态空间模型（SSM）Mamba，具有线性推理复杂度和上下文感知推理能力，为解决上述问题提供了新思路。
- **核心问题**：能否开发一个高效的机器人VLA模型，既具备强大的推理能力，又能以极小代价获得操作技能？
- **整体含义**：论文提出RoboMamba，旨在利用Mamba的线性复杂度特性，构建一个端到端的高效VLA模型，在保持推理与操作能力的同时，显著降低微调参数和推理时间，推动VLA模型在机器人领域的实际部署。

---

### 论文提出的方法论：核心思想、关键技术细节

#### 核心思想
- 采用Mamba作为语言模型，与视觉编码器结合，构建高效VLA架构。
- 通过**两阶段训练**：第一阶段使模型获得视觉常识和机器人相关推理能力；第二阶段通过**高效微调**（仅微调0.1%参数）赋予模型6自由度（SE(3)）姿态预测能力。
- 关键发现：一旦模型具备足够强的推理能力，就能以极低的代价快速学会操作技能。

#### 总体架构
- **视觉编码器**：CLIP ViT-Large（224x224或336x336输入），提取视觉特征。
- **投影层**：简单MLP，将视觉特征映射到Mamba语言模型的embedding空间。
- **语言模型**：Mamba（2.8B或1.4B参数），采用选择性状态空间模型（S6），实现线性时间复杂度。
- **策略头**：操作微调阶段时，冻结整个预训练模型，注入两个轻量MLP头（共3.7M参数，占模型0.1%），分别预测末端执行器的位置（3维）和方向（3x3旋转矩阵）。
- 输出：模型可同时生成自然语言响应（推理）和通过策略头输出动作姿态。

#### 训练流程（文字描述）
1.  **Stage1.1：对齐预训练**
    - 数据：LLaVA-LCS 558K图像-文本对。
    - 冻结视觉编码器和Mamba，仅更新投影层，使视觉特征与文本嵌入对齐。
    - 目标：跨模态对齐。
2.  **Stage1.2：指令协同训练**
    - 数据：通用视觉指令数据（如LLaVA 1.5 655K、ShareGPT4V-SFT、LLaVA-Next）与机器人指令数据（RoboVQA 300K）混合。
    - 冻结CLIP编码器，微调投影层和Mamba。
    - 损失函数：交叉熵损失，监督语言输出。
    - 目的：增强模型在通用场景和机器人场景下的推理能力。
3.  **Stage2：机器人操作微调**
    - 数据：在SAPIEN仿真环境中收集的10K张图像及其对应的成功操作姿态。
    - 冻结整个Stage1模型参数，仅训练策略头。
    - 损失函数：位置损失使用L1损失；方向损失使用旋转矩阵的arccos损失（公式(5)(6)）。
    - 输出：预测接触点的2D位置（结合深度转换为3D）和3D旋转矩阵。

---

### 实验设计：数据集、Benchmark和对比方法

#### 数据集
- **Stage1.1**：LLaVA-LCS 558K。
- **Stage1.2**：通用指令数据（LLaVA 1.5 655K，或其他如ShareGPT4V-SFT、LLaVA-Next）+ 机器人指令数据（RoboVQA 300K）。
- **Stage2**：使用SAPIEN引擎生成的10K训练样本（20个操作类别，如门、冰箱、微波炉等），测试集1.1K样本（包含20个训练类别和10个未见类别）。
- **真实世界**：使用Franka Panda机器人操作日常物体，进行定性评估。

#### Benchmark（评估指标）
- **通用推理能力**：OKVQA, VQAv2, GQA, VizWiz, POPE, MME, MMBench, MM-Vet。
- **机器人相关推理能力**：RoboVQA验证集（BLEU-1~BLEU-4分数），评估任务规划、成功分类、属性预测等。
- **操作能力**：在SAPIEN仿真中测试开放循环的任务完成成功率（定义：物体关节状态变化超过0.1米为成功）。报告在20个seen类别和10个unseen类别上的平均准确率。

#### 对比方法
- **通用推理**：BLIP-2, InstructBLIP, LLaMA-AdapterV2, MiniGPT-v2, Qwen-VL, LLaVA1.5, SPHINX, LLaVA-Phi, MobileVLM, TinyLLaVA等。
- **机器人推理**：LLaMA-AdapterV2和TinyLLaVA（在RoboVQA上微调后对比）。
- **操作**：UMPNet, FlowBot3D, RoboFlamingo, ManipLLM（所有基线均使用作者收集的相同数据重新训练）。

---

### 资源与算力

- **硬件**：所有实验在单个NVIDIA A100 GPU上运行（论文未明确说明GPU数量，推测为单卡）。
- **训练时间**：Stage1.1（对齐预训练）：1个epoch；Stage1.2（指令协同训练）：2个epochs；Stage2（操作微调）：8个epochs，仅需“数十分钟”（a few dozen minutes）。
- **精度与优化器**：Stage1使用16-bit浮点，Stage2使用32-bit浮点。优化器为AdamW（β1=0.9, β2=0.999），学习率4e-5（Stage1）或1e-5（Stage2），权重衰减0.1（Stage2）。
- **模型规模**：总参数量约2.8B（2.7B语言模型+视觉编码器），微调参数仅3.7M（0.1%）。

---

### 实验数量与充分性

- **实验数量**：论文进行了大量实验：
    - 通用推理对比：1个主表（Table1），与10+个MLLM在9个benchmark上对比。
    - 机器人推理对比：在RoboVQA上对比2个基线。
    - 操作成功率对比：主表（Table2）涵盖20个seen任务和10个unseen任务，与4个基线对比。
    - 消融实验：图3（LLM影响、推理能力影响）、附录C（图像编码器、训练数据集、策略头设计）共7个消融实验。
    - 真实世界定性实验：多个任务展示（图4,5,6）。
- **充分性与公平性**：
    - **充分性**：实验覆盖了推理和操作两大能力，并在仿真和真实场景评估。消融实验系统性地验证了关键设计（LLM选择、推理能力对操作的影响、数据组成、策略头设计）。
    - **公平性**：在操作实验中，所有基线均使用相同的数据集重新训练。在推理对比中，RoboVQA上的机器人推理对比，也微调了基线（LLaMA-AdapterV2和TinyLLaVA）以确保公平。
    - **不足之处**：未报告多次试验的统计误差（如标准差或置信区间）；部分对比（如通用推理）使用的输入分辨率不同，可能影响公平性；未提及真实的工业级部署测试。

---

### 论文的主要结论与发现

1.  **高效性**：RoboMamba实现了显著的计算效率。推理速度是现有VLA模型的3倍（9.0 Hz vs OpenVLA的1.1 Hz）；微调参数仅0.1%（3.7M），训练时间仅数十分钟。
2.  **强推理能力**：在通用推理benchmark上，RoboMamba（2.7B语言模型）表现与7B级别的MLLM相当或更优；在机器人推理（RoboVQA）上，以BLEU-4 42.8分超过LLaMA-AdapterV2等基线。
3.  **推理能力对操作学习的关键性**：实验表明，一旦模型具备强大的机器人类别推理能力，仅需极小的操作微调参数即可学会姿态预测。推理能力越强，操作成功率越高。
4.  **协同训练的有效性**：通用指令数据与机器人指令数据的联合训练（Stage1.2）不仅增强了机器人推理，也提升了通用场景的推理能力（空间识别等）。
5.  **SOTA操作性能**：在SAPIEN仿真中，RoboMamba在seen任务上平均成功率达到63.7%（比ManipLLM高7%），在unseen任务上平均53%（比ManipLLM高2%）。

---

### 优点：方法与实验设计的亮点

1.  **技术创新**：首个将Mamba（状态空间模型）应用于机器人VLA模型的工作，利用其线性复杂度实现高效推理。
2.  **极简高效微调**：发现强大的推理能力可以“迁移”到动作预测，仅需微调极轻量头（0.1%参数），避免了传统VLA模型因微调LLM带来的灾难性遗忘和高成本。
3.  **全面的训练策略**：设计了两阶段训练策略，并创新性地引入机器人指令数据的协同训练，显著提升推理能力。
4.  **系统性的消融实验**：不仅验证了模型设计各部件的作用，还深入揭示了推理能力与操作性能之间存在正相关关系，提供了有价值的见解。
5.  **实际验证**：在仿真和真实机器人上均进行了验证，展示了方法的实用性。

---

### 不足与局限

1.  **模型规模限制**：当前模型基于2.7B语言模型，在一些复杂推理任务（如MM-Vet）上仍落后于基于7B/13B LLM的MLLM（如LLaVA-1.5, SPHINX）。
2.  **输入模态单一**：依赖2D RGB-D图像，缺乏3D点云或时间序列信息，可能限制对精细操作和动态环境的适应能力。作者也指出未来计划构建4D（3D+时间）机器人VLA模型。
3.  **评估范围有限**：操作评估仅在SAPIEN仿真中测试开放循环的成功率，未进行多回合闭环操作或真实重复性实验。真实世界实验仅提供定性结果，缺乏定量指标。
4.  **潜在偏差风险**：训练数据主要来自仿真和特定数据集（PartNet-Mobility），泛化到真实世界复杂、非结构化场景的能力有待验证。机器人推理数据（RoboVQA）可能存在场景分布偏差。
5.  **未报告统计稳定性**：多数实验结果未附带误差条或置信区间，无法判断结果的可重复性和稳定性。
6.  **策略头设计局限性**：采用的简单MLP策略头可能不足以学习复杂的、序列相关的操作策略。

---

（完）
