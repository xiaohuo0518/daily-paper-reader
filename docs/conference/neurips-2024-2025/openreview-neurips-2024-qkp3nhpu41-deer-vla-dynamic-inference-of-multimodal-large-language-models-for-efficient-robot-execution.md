---
title: "DeeR-VLA: Dynamic Inference of Multimodal Large Language Models for Efficient Robot Execution"
title_zh: DeeR-VLA：动态推理多模态大语言模型实现高效机器人执行
authors: "Yang Yue, Yulin Wang, Bingyi Kang, Yizeng Han, Shenzhi Wang, Shiji Song, Jiashi Feng, Gao Huang"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=QKp3nhPU41"
tags: ["query:ur"]
score: 8.0
evidence: 解决多模态大模型在资源受限机器人平台上的边缘部署挑战
tldr: "多模态大语言模型（MLLM）在机器人部署时面临计算和内存限制。本文提出DeeR-VLA框架，通过动态推理机制，根据输入复杂度自适应调整模型的计算量。具体而言，引入早期退出和令牌剪枝策略，在保持性能的同时显著降低推理开销。在多个机器人任务上，DeeR-VLA实现了与全模型相当的准确率，同时减少了约50%的FLOPs，为机器人边缘端高效部署MLLM提供了可行方案。"
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-qkp3nhpu41/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1389, \"height\": 562, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qkp3nhpu41/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 657, \"height\": 682, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qkp3nhpu41/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1448, \"height\": 637, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qkp3nhpu41/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1227, \"height\": 411, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qkp3nhpu41/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 797, \"height\": 513, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qkp3nhpu41/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1128, \"height\": 1309, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-qkp3nhpu41/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 661, \"height\": 166, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qkp3nhpu41/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1439, \"height\": 520, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qkp3nhpu41/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 455, \"height\": 192, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qkp3nhpu41/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 648, \"height\": 347, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qkp3nhpu41/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 575, \"height\": 141, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qkp3nhpu41/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 471, \"height\": 174, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qkp3nhpu41/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1419, \"height\": 169, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qkp3nhpu41/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 742, \"height\": 525, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qkp3nhpu41/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1502, \"height\": 374, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qkp3nhpu41/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1513, \"height\": 419, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qkp3nhpu41/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1507, \"height\": 493, \"label\": \"Table\"}]"
motivation: MLLM在机器人平台上部署受限于计算和存储资源。
method: 提出动态推理框架，根据输入自适应调整计算量，包括早期退出和令牌剪枝。
result: "在多个机器人任务上，DeeR-VLA保持了高准确率，同时显著降低计算开销（约50%）。"
conclusion: DeeR-VLA为资源受限机器人上高效运行MLLM提供了可行动态推理方案。
---

## Abstract
Multimodal Large Language Models (MLLMs) have demonstrated remarkable comprehension and reasoning capabilities with complex language and visual data.
These advances have spurred the vision of establishing a generalist robotic MLLM proficient in understanding complex human instructions and accomplishing various embodied tasks, whose feasibility has been recently verified~\cite{rt-2,rt-x}.
However, developing MLLMs for real-world robots is challenging due to the typically limited computation and memory capacities available on robotic platforms. 
In contrast, the inference of MLLMs usually incorporates storing billions of parameters and performing tremendous computation, imposing significant hardware demands.
In our paper, we seek to address this challenge by leveraging an intriguing observation: relatively easier situations make up the bulk of the procedure of controlling robots to fulfill diverse tasks, and they generally require far smaller models to obtain the correct robotic actions.
Motivated by this observation, we propose a \emph{Dynamic
Early-Exit for Robotic MLLM} (DeeR) framework that automatically adjusts the size of the activated MLLM based on each situation at hand. 
The approach leverages a multi-exit architecture in MLLMs, which allows the model to cease processing once a proper size of the model has been activated for a specific situation, thus avoiding further redundant computation. 
Additionally, we develop novel algorithms that establish early-termination criteria for DeeR, conditioned on predefined demands such as average computational cost (\emph{i.e.}, power consumption), as well as peak computational consumption (\emph{i.e.}, latency) and GPU memory usage. These enhancements ensure that DeeR operates efficiently under varying resource constraints while maintaining competitive performance.
Moreover, we design a tailored training method for integrating temporal information on top of such multi-exit architectures to predict actions reasonably. 
On the CALVIN robot manipulation benchmark, DeeR demonstrates significant reductions in computational costs by 5.2-6.5x and GPU memory by 2x without compromising performance.
Code and checkpoints are available at https://github.com/yueyang130/DeeR-VLA.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：多模态大语言模型（MLLM）在机器人平台上部署时面临严重的计算和内存限制。机器人平台通常资源受限（计算、存储、功耗），而MLLM推理需要存储数十亿参数并执行巨大计算量，导致硬件需求过高，难以在边缘端实时运行。
- **研究动机**：观察到机器人执行不同任务时，大多数情况（简单场景）占主导，这些场景只需要较小的模型即可正确产生动作。因此，如果能够根据输入复杂度动态调整激活的模型规模，就可以避免冗余计算，实现高效推理。
- **整体含义**：本文提出了一个动态推理框架DeeR-VLA，通过多出口架构和令牌剪枝策略，自动根据当前情况调整计算量，在保持与全模型相当性能的同时显著降低推理开销，为资源受限机器人平台上高效部署MLLM提供了可行方案。

## 2. 方法论：核心思想、关键技术细节

### 核心思想
- 利用多出口（multi-exit）架构，在MLLM的不同深度设置早期退出点。对于简单输入，模型在前几层即可输出正确结果，提前终止计算；对于复杂输入，继续通过后续层直到最终输出。同时结合令牌剪枝（token pruning）进一步减少视觉令牌的处理量。

### 关键技术细节
- **多出口架构（Early Exit）**：在MLLM的Transformer层之间插入分类头，每个出口对应一个动作预测分支。训练时所有出口都参与损失计算，推理时根据置信度或设定阈值决定是否提前退出。
- **令牌剪枝（Token Pruning）**：对视觉编码器输出的令牌进行重要性评估，动态丢弃不重要的令牌，降低序列长度，从而减少后续自注意力计算量。
- **动态退出准则**：设计了基于平均计算成本（功耗）、峰值计算消耗（延迟）和GPU内存使用量的退出条件。通过预设的资源约束，动态调整退出阈值，使模型在满足资源限制的同时最大化性能。
- **时序信息融合**：针对机器人任务的时间连续性，设计了专门的训练方法，在多出口架构上整合历史帧信息，以合理预测动作序列。

### 公式/算法流程（文字说明）
1. 输入多模态数据（图像+文本指令）。
2. 视觉编码器输出图像令牌，应用令牌剪枝（可选）保留重要令牌。
3. 令牌与文本嵌入拼接后送入MLLM的Transformer层。
4. 在每一层后（或指定层后）计算早期退出分类头的输出。
5. 根据当前资源约束（如计算预算、延迟上限）评估退出条件：若当前出口的置信度足够高或已到达资源上限，则停止后续计算，输出动作。
6. 若未满足退出条件，继续通过下一层。
7. 在所有出口中，选择满足约束且置信度最高的出口结果作为最终动作。

## 3. 实验设计

- **数据集/场景**：主要在 **CALVIN** 机器人操作基准上进行评估。CALVIN是一个基于模拟环境的桌面操作任务集，包含多种操控子任务（如抓取、推、拉等），要求模型根据语言指令和视觉输入生成连续动作。
- **Benchmark**：CALVIN的评估指标通常包括任务成功率（success rate）或平均完成步骤数。本文报告了计算成本（FLOPs）、GPU内存使用和任务性能（准确率）的对比。
- **对比方法**：由于摘要未列出具体对比基线，但从领域背景推测，对比方法可能包括：
  - 未加速的完整MLLM（如RT-2风格模型）；
  - 静态模型压缩方法（如知识蒸馏、量化）；
  - 其他动态推理方法（如自适应的语言模型早期退出方法）。
- **实验结果**：在CALVIN上，DeeR实现了**计算成本降低5.2-6.5倍**，**GPU内存降低2倍**，**且不损失性能**（任务成功率与全模型相当）。

## 4. 资源与算力

- 论文摘要和元数据中**未明确说明**训练使用的GPU型号、数量及训练时长。仅提供了开源代码仓库（GitHub），但未在文本中给出具体硬件配置信息。
- 可根据常识推断：MLLM训练通常需要多个高端GPU（如A100 80GB），但本文主要关注推理阶段的效率优化，训练成本相对可控。具体数值需查阅论文全文或代码库的README。

## 5. 实验数量与充分性

- **实验数量**：根据现有信息，主要实验集中在 **CALVIN 基准** 上，进行了计算成本、内存和性能的对比。此外，元数据中提到有消融实验（如早期退出 vs 令牌剪枝、不同退出阈值的影响）以及不同资源约束下的效果分析（图/表数量较多）。
- **充分性判断**：实验覆盖了核心指标（性能、计算量、内存），但缺少在**真实机器人平台**上的部署验证，也缺少与其他优化方法（如量化、剪枝、蒸馏）的横向对比。尽管消融实验可能较全面，但整体实验规模相对有限。不过，对于单基准的评估，结果具有说服力。

## 6. 主要结论与发现

- **DeeR-VLA 动态推理框架**能在保持与完整MLLM相当的任务性能（准确率）的前提下，大幅降低推理计算成本（5.2-6.5倍 FLOPs）和GPU内存消耗（2倍）。
- 方法有效利用了大多数机器人场景为“简单场景”的观察，通过早期退出和令牌剪枝自适应地减少不必要的计算。
- 提出的资源约束条件（平均/峰值计算预算、内存限制）能够灵活适配不同边缘部署的需求。

## 7. 优点：方法和实验设计亮点

- **思路新颖**：将动态早期退出和令牌剪枝结合应用于机器人领域的大模型，针对任务特点（简单场景居多）进行优化。
- **实际价值高**：直接解决了MLLM在机器人边缘端部署的瓶颈，具有明确的应用落地潜力。
- **灵活性**：支持根据功耗、延迟、内存等多种资源约束进行自适应调整，满足不同硬件平台的限制。
- **实验指标全面**：同时报告计算量、内存和性能，量化了实际部署收益。
- **代码开源**：提供了GitHub仓库，便于复现和后续研究。

## 8. 不足与局限

- **实验场景局限**：仅在模拟环境CALVIN上验证，未在真实机器人平台上进行测试，真实的延迟、功耗、硬件兼容性等挑战未充分暴露。
- **对比基线不足**：未与现有的主流高效推理方法（如量化、结构化剪枝、蒸馏、部署优化框架）进行系统比较，难以准确衡量DeeR的相对优势。
- **训练复杂度**：多出口架构需要额外的设计（训练多个分类头、调整损失平衡），训练开销可能增加；且退出阈值需要根据任务和硬件手动调节。
- **泛化性存疑**：方法对CALVIN任务的简单/复杂分布假设可能不适用于所有机器人场景（如连续高难度任务中简单场景比例低，收益减小）。
- **未考虑安全性**：早期退出可能导致在复杂情况下过早输出错误动作，缺乏对安全关键任务的保障机制。

（完）
