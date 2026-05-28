---
title: "A Large Recurrent Action Model: xLSTM enables Fast Inference for Robotics Tasks"
title_zh: 大型循环动作模型：xLSTM实现机器人任务的快速推理
authors: "Thomas Schmied, Thomas Adler, Vihang Prakash Patil, Maximilian Beck, Korbinian Pöppel, Johannes Brandstetter, Günter Klambauer, Razvan Pascanu, Sepp Hochreiter"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=J2JxJ0P1LI"
tags: ["query:ur"]
score: 6.0
evidence: 快速推理适用于机器人实时应用
tldr: 该论文针对Transformer在机器人实时任务中推理速度慢的问题，提出了基于xLSTM的大型循环动作模型。该模型在保持训练并行化的同时大幅提升推理速度，实验表明在多种机器人任务上性能与Transformer相当但速度更快，为机器人边缘端部署提供了高效的模型架构。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1344, \"height\": 544, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1345, \"height\": 630, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1121, \"height\": 467, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 834, \"height\": 477, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 830, \"height\": 518, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1729, \"height\": 527, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 735, \"height\": 501, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1562, \"height\": 430, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1562, \"height\": 385, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 904, \"height\": 1647, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1127, \"height\": 1032, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 862, \"height\": 607, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1299, \"height\": 625, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 862, \"height\": 582, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1249, \"height\": 518, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1295, \"height\": 622, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1298, \"height\": 576, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1300, \"height\": 573, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1303, \"height\": 572, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1305, \"height\": 573, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1514, \"height\": 601, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 671, \"height\": 518, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1294, \"height\": 608, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1296, \"height\": 614, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1163, \"height\": 1039, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1299, \"height\": 617, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 1158, \"height\": 553, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 1298, \"height\": 619, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 1297, \"height\": 618, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-030.webp\", \"caption\": \"\", \"page\": 0, \"index\": 30, \"width\": 1300, \"height\": 656, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-031.webp\", \"caption\": \"\", \"page\": 0, \"index\": 31, \"width\": 1289, \"height\": 650, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-032.webp\", \"caption\": \"\", \"page\": 0, \"index\": 32, \"width\": 1296, \"height\": 627, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-033.webp\", \"caption\": \"\", \"page\": 0, \"index\": 33, \"width\": 1299, \"height\": 615, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-j2jxj0p1li/fig-034.webp\", \"caption\": \"\", \"page\": 0, \"index\": 34, \"width\": 1642, \"height\": 651, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-j2jxj0p1li/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1445, \"height\": 425, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j2jxj0p1li/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 950, \"height\": 1531, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j2jxj0p1li/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1201, \"height\": 638, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j2jxj0p1li/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1055, \"height\": 680, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j2jxj0p1li/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 814, \"height\": 747, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j2jxj0p1li/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 990, \"height\": 693, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j2jxj0p1li/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1130, \"height\": 142, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j2jxj0p1li/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1047, \"height\": 682, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j2jxj0p1li/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1198, \"height\": 1962, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j2jxj0p1li/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1402, \"height\": 1646, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j2jxj0p1li/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1413, \"height\": 595, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j2jxj0p1li/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 863, \"height\": 2155, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j2jxj0p1li/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1386, \"height\": 2193, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j2jxj0p1li/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1388, \"height\": 2204, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j2jxj0p1li/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1395, \"height\": 2117, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-j2jxj0p1li/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1394, \"height\": 1609, \"label\": \"Table\"}]"
motivation: Transformer模型在机器人实时任务中因推理速度慢而难以实际应用，亟需更高效的架构。
method: 采用xLSTM现代循环架构构建大型动作模型，在离线数据集上通过序列建模训练实现快速推理。
result: 在多个机器人仿真和真实任务中，xLSTM模型推理速度远超Transformer且任务性能相近。
conclusion: xLSTM循环架构为机器人实时控制和边缘部署提供了高效可行的替代方案。
---

## Abstract
In recent years, there has been a trend in the field of Reinforcement Learning (RL) towards large action models trained offline on large-scale datasets via sequence modeling. Existing models are primarily based on the Transformer architecture, which results in powerful agents. However, due to slow inference times, Transformer-based approaches are impractical for real-time applications, such as robotics. Recently, modern recurrent architectures, such as xLSTM and Mamba, have been proposed that exhibit parallelization benefits during training similar to the Transformer architecture while offering fast inference. In this work, we study the aptitude of these modern recurrent architectures for large action models. Consequently, we propose a Large Recurrent Action Model (LRAM) with an xLSTM at its core that comes with linear-time inference complexity and natural sequence length extrapolation abilities. Experiments on 432 tasks from 6 domains show that LRAM compares favorably to Transformers in terms of performance and speed.

---

## 论文详细总结（自动生成）

# 论文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **问题**：大型动作模型（LAM）通常基于Transformer架构，虽然训练时可高效并行，但在推理时因自注意力机制的平方复杂度导致速度慢、内存占用高，难以满足机器人等实时应用对低延迟（如10ms以内）的要求。
- **背景**：强化学习领域正从在线训练转向基于大规模离线数据集和序列建模的训练方式。Transformer驱动的LAM（如Decision Transformer、Gato）性能强大，但推理效率是部署瓶颈。
- **目标**：探索现代循环架构（xLSTM、Mamba）作为LAM骨干的可行性，利用其线性推理复杂度和自然的长序列外推能力，在保持训练并行性的同时大幅提升推理速度。

## 2. 论文提出的方法论
### 核心思想
- 构建**大型循环动作模型（Large Recurrent Action Model, LRAM）**，以xLSTM为核心，也可替换为Mamba。模型采用与Decision Transformer类似的离线行为克隆训练方式，但使用循环推理模式（保持隐藏状态），实现每步常量时间推理。
### 关键技术细节
- **多模态序列表示**：对图像使用CNN编码，对低维状态使用全连接层；不采用图像分块或状态离散化，避免序列过长。序列仅包含状态、回报-去（RTG）、奖励，**不包含动作**（实验发现避免“复制猫问题”可提升性能）。
- **共享动作头**：将连续动作离散化为256个均匀间隔的bin，离散动作和连续动作维度统一用共享的分类头预测（最大类别数2066），避免自回归预测，加速推理。
- **循环推理模式**：推理时只保留上一时刻隐藏状态，无需重新处理整个序列，复杂度为O(T)（线性），而Transformer即使使用KV缓存每步复杂度也随上下文长度线性增长（总复杂度二次）。
- **训练**：使用交叉熵损失，各领域按均匀比例采样，批量大小128，梯度累积6，学习率1e-4余弦衰减，AdamW优化器，梯度裁剪0.25，权重衰减0.01，不使用dropout（发现有害）。
- **模型变体**：对比xLSTM [7:1]（7个mLSTM+1个sLSTM）、xLSTM [1:0]（全mLSTM）、Mamba、GPT-2风格Transformer（DT）。参数规模从16M到206M，xLSTM和Mamba使用Transformer两倍层数以匹配参数量。

## 3. 实验设计
### 数据集与场景
- **总规模**：432个训练任务，来自6个领域，共894M transitions，3.4M条轨迹。另保留37个hold-out任务用于零样本评估。
- **各领域**：
  - Atari（41训练+5 hold-out）：206M transitions，DQN-Replay数据，图像观测，离散动作。
  - Composuite（240训练+16 hold-out）：240M transitions，机器人操作，状态观测，连续动作。
  - DMControl（11训练+5 hold-out）：110M transitions，自生成SAC数据，连续动作。
  - Meta-World（45训练+5 hold-out）：90M transitions，来自Schmied等2024，连续动作。
  - Mimicgen（83训练+2 hold-out）：25M transitions，来自Mandlekar等2023及自生成，连续动作。
  - Procgen（12训练+4 hold-out）：224M transitions，来自Schmied等2024b，图像观测，离散动作。
### 基准方法
- **对比方法**：xLSTM [7:1]、xLSTM [1:0]、Mamba、DT（Decision Transformer）。所有方法使用相同编码器、动作头、训练超参数。
### 评估指标
- 序列预测：验证集困惑度（perplexity）。
- 任务性能：各领域归一化得分（人归一化或数据归一化），Atari使用人归一化。
- 推理速度：延迟（秒/步）和吞吐量（步/秒），在A100-40GB上测试，使用Atari Freeway（最长序列8192步）。
- 额外分析：微调性能、上下文学习（ICL，Dark-Room环境）、嵌入空间聚类（UMAP）。

## 4. 资源与算力
- **硬件**：4×A100 GPU（40GB显存每卡），使用分布式数据并行（DDP）。
- **训练时间**：最小模型（16M）约5小时，最大模型（206M Mamba）约30小时。所有训练使用混合精度（PyTorch AMP）。
- **评估**：并行4进程每GPU，全部432任务评估耗时18分钟到2小时不等。
- **文中未明确说明总GPU时数或能耗**，但提供了模型规模和训练时间范围。

## 5. 实验数量与充分性
- **主要实验**：4种骨干×4种模型规模（16M/48M/110M/206M）=16个组合，每个组合3个种子，重复验证。
- **消融实验**：
  - 移除输入动作的影响（5种上下文长度）。
  - 移除RTG/奖励条件（行为克隆设置）。
  - mLSTM/sLSTM比例（6种不同配置）。
  - 减少xLSTM层数的影响。
  - Dropout对DT的影响。
  - 上下文长度对xLSTM的影响（5种长度）。
- **推理速度对比**：延迟/吞吐量测试包括多种批次大小、上下文长度、头维度。
- **充分性评估**：
  - 实验覆盖6个差异大的领域（游戏、机器人操作、控制），任务数多。
  - 零样本泛化（37个hold-out任务）和微调实验验证迁移能力。
  - ICL实验在Dark-Room上进行（80训练+20测试位置）。
  - 统计显著性：报告均值及95%置信区间（3个种子），符合Agarwal等2021建议。
- **客观公平性**：所有方法使用相同序列表示、训练超参数、评估协议；推理速度对比使用相同参数规模的模型（调整层数匹配参数量），使用KV缓存和FlashAttention加速Transformer，使用定制内核加速xLSTM。

## 6. 主要结论与发现
1.  **性能**：xLSTM和Mamba在各个模型规模上验证困惑度和任务得分均优于Transformer。在206M规模，xLSTM [7:1]和[1:0]平均归一化得分最高，Mamba次之，DT最低。
2.  **推理速度**：
   - 延迟：对于长上下文（>800步），xLSTM和Mamba显著快于DT（DT在上下文大时OOM）。在batch=1且上下文=25600步时，xLSTM比DT快约10倍。
   - 吞吐量：xLSTM和Mamba在大批次下吞吐量远高于DT（DT在batch>64时OOM）。
3.  **消融发现**：
   - 移除输入中的动作可大幅提升连续控制域性能（避免复制猫问题），且长上下文更有益。
   - 移除RTG/奖励不影响骨干相对排名。
   - sLSTM块在状态跟踪任务（Dark-Room ICL）中提供额外好处；在大多数观测完全的任务中mLSTM即可。
   - Dropout对DT有害，实验中禁用。
4.  **泛化**：预训练LRAM在hold-out任务微调优于随机初始化；ICL性能上xLSTM [7:1]最优（因sLSTM的状态跟踪能力）。
5.  **嵌入空间**：xLSTM的UMAP聚类显示比DT更清晰的域分离，可能有助于任务识别。

## 7. 优点
- **创新性**：首次系统评估现代循环架构（xLSTM、Mamba）作为大型动作模型骨干，提出LRAM并验证其在机器人相关任务中的有效性。
- **实用性**：线性推理复杂度使其非常适合边缘设备、实时控制、长上下文（如ICL需要多回合经验），直接解决了Transformer在机器人部署中的关键瓶颈。
- **实验严谨性**：大规模多域数据集（894M transitions），覆盖432任务；多种模型规模、充分消融、统计显著性报告；推理速度对比详细（不同batch、上下文长度、头维度、内核加速对比）。
- **开源贡献**：释放数据准备管道和数据集（GitHub），促进可复现研究。
- **设计细节**：共享动作头、移除输入动作、不使用位置编码等创新点实际提升了性能/速度。

## 8. 不足与局限
- **未包含真实机器人实验**：所有实验在模拟环境中进行（Atari、Procgen、Meta-World、DMControl、Composuite、Mimicgen），虽然面向机器人，但缺乏真实机器人验证，结论向真实世界的泛化性尚未确认。
- **微调限于离线**：微调实验仅使用离线数据（选择最优5%轨迹），未探索在线RL微调，而在线微调可能是预训练模型的关键应用。
- **ICL实验简单**：仅在Dark-Room（10×10网格世界）上进行，环境较简单，未在复杂机器人任务上验证ICL能力。
- **模型规模有限**：最大模型206M参数，相比现代LLM规模（数十亿）较小，更大模型下的趋势和可扩展性还不确定（仅有一个408M单次运行）。
- **计算资源未详细报告**：未提供总GPU小时、能耗等，不利于复现成本评估。
- **潜在偏差**：数据集主要来自模拟和公开数据（如DQN-Replay、SAC生成），可能不包含真实世界分布的多样性；任务选择可能偏向论文作者团队之前的工作。
- **公平性局限**：推理速度对比中Mamba因与torch.compile不兼容而在batch=1时比DT慢，虽预期兼容后可改善，但仍影响直接比较的公平性。

（完）
