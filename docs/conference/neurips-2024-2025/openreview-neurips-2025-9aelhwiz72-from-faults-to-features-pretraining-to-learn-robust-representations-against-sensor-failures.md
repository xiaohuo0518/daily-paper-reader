---
title: "From Faults to Features: Pretraining to Learn Robust Representations against Sensor Failures"
title_zh: 从故障到特征：通过预训练学习针对传感器故障的鲁棒表示
authors: "Jens U. Brandt, Noah C. Pütz, Marcus Greiff, Thomas Jonathan Lew, John Subosits, Marc Hilbert, Thomas Bartz-Beielstein"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=9aElHWiZ72"
tags: ["query:ur"]
score: 9.0
evidence: 针对传感器故障的预训练鲁棒表示，可应用于人形机器人故障诊断
tldr: 传感器故障会导致安全关键系统失效。本文提出一种预训练方法，通过专门针对传感器中断的掩码策略，学习对传感器故障鲁棒的表示，在不增加推理成本的前提下提升模型在缺失输入下的可靠性，其思想可直接迁移至人形机器人故障诊断场景。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1441, \"height\": 423, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1435, \"height\": 325, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1311, \"height\": 486, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1378, \"height\": 1158, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 657, \"height\": 285, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1453, \"height\": 874, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1443, \"height\": 1286, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1434, \"height\": 529, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1436, \"height\": 471, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1436, \"height\": 467, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1434, \"height\": 527, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1431, \"height\": 1989, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1445, \"height\": 1290, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1449, \"height\": 1107, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1450, \"height\": 1092, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1444, \"height\": 1108, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1438, \"height\": 963, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1443, \"height\": 971, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1405, \"height\": 1182, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1440, \"height\": 675, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1418, \"height\": 738, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1330, \"height\": 621, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1325, \"height\": 620, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1173, \"height\": 737, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1301, \"height\": 1500, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1297, \"height\": 1103, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 1301, \"height\": 1101, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 1301, \"height\": 1101, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9aelhwiz72/fig-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 1293, \"height\": 1101, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-9aelhwiz72/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1386, \"height\": 299, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9aelhwiz72/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1181, \"height\": 420, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9aelhwiz72/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 637, \"height\": 217, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9aelhwiz72/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1130, \"height\": 338, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9aelhwiz72/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1195, \"height\": 218, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9aelhwiz72/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 599, \"height\": 745, \"label\": \"Table\"}]"
motivation: 安全关键系统中传感器故障会导致模型严重失效，现有预训练方法未专门针对传感器中断。
method: 提出面向传感器中断的掩码预训练策略，学习鲁棒表示。
result: 在自动驾驶数据集上，该方法显著提升传感器故障下的模型性能。
conclusion: 针对传感器故障的预训练可有效提升系统鲁棒性。
---

## Abstract
Machine learning models play a key role in safety-critical applications, such as autonomous vehicles and advanced driver assistance systems, where their robustness during inference is essential to ensure reliable operation. Sensor faults, however, can corrupt input signals, potentially leading to severe model failures that compromise reliability. In this context, pretraining emerges as a powerful approach for learning expressive representations applicable to various downstream tasks. Among existing techniques, masking represents a promising direction for learning representations that are robust to corrupted input data. In this work, we extend this concept by specifically targeting robustness to sensor outages during pretraining. We propose a self-supervised masking scheme that simulates common sensor failures and explicitly trains the model to recover the original signal. We demonstrate that the resulting representations significantly improve the robustness of predictions to seen and unseen sensor failures on a vehicle dynamics dataset, maintaining
strong downstream performance under both nominal and various fault conditions. As a practical application, we deploy the method on a modified Lexus LC 500 and show that the pretrained model successfully operates as a substitute for a physical sensor in a closed-loop control system. In this autonomous racing application, a supervised baseline trained without sensor failures may cause the vehicle to leave the track. In contrast, a model trained using the proposed masking scheme enables reliable racing performance in the presence of sensor failures.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：在安全关键系统（如自动驾驶、机器人）中，传感器故障（如偏置、漂移、硬故障、噪声等）会导致机器学习模型输入分布偏移，引发严重性能下降甚至系统失效。现有自监督预训练方法（如随机掩码）虽然能学习鲁棒表示，但其掩码模式（如置零）与真实传感器故障（如持续偏置、漂移）差异较大，导致实际场景中模型仍然脆弱。
- **研究含义**：本文提出一种**专门针对传感器中断的预训练掩码策略**，通过在预训练阶段模拟真实故障模式使模型学会重构原始信号，从而在不增加推理成本的前提下显著提升下游模型对多种传感器故障的鲁棒性。

## 2. 论文提出的方法论

### 核心思想
将预训练从简单的随机掩码（置零）扩展为**多种传感器故障模拟**，形成一个多任务重建目标。模型学习将带故障的输入投影回数据流形（manifold），从而获得对类似扰动的内在鲁棒性。

### 关键技术细节
- **输入数据**：多元时间序列，形状为 \( \mathbf{X} \in \mathbb{R}^{B \times S \times F} \)，\( B \) 为批次大小，\( S \) 为序列长度，\( F \) 为通道数。
- **多任务掩码**：将每个批次划分为 \( n \) 个子批次，每个子批次对应一种故障掩码函数 \( D_i \)。本文采用 \( n=3 \) 种掩码：
  1. **Mean masking**（硬故障）：将掩码位置置为该通道均值（归一化后即为0）。公式：\(\tilde{\mathbf{X}}_i = \mathbf{X}_i \odot \mathbf{M}_i\)。
  2. **Bias masking**（偏置故障）：向掩码位置添加常数偏移 \( C_{b,f} \sim \mathcal{U}(l\sigma[f], u\sigma[f]) \)，且所有时间步共享同一偏移。公式：\(\tilde{\mathbf{X}}_i = \mathbf{X}_i + \mathbf{C}_i \odot (1 - \mathbf{M}_i)\)。
  3. **Noise masking**（噪声故障）：向掩码位置添加零均值高斯噪声，方差 \( r\sigma^2[f] \)。公式与Bias masking相同（但噪声张量各元素独立）。
- **掩码生成**：采用几何分布采样策略（源自Zerveas et al. 2021），控制掩码比率 \( m_r=0.1 \) 和平均掩码块长度 \( l_m=20 \)（即平均掩码整个通道）。
- **损失函数**：仅计算掩码位置上的均方误差（MSE），不要求重构可见部分。 \[
  \mathcal{L} = \sum_{i=1}^{n} \frac{1}{|\mathcal{M}_i|} \sum_{(b,s,f) \in \mathcal{M}_i} \left( [\mathbf{X}_i]_{b,s,f} - [\hat{\mathbf{X}}_i]_{b,s,f} \right)^2
  \]
- **模型架构**：
  - 编码器 \( E \)：基于Transformer（4层，嵌入维度512，16注意力头，前馈2048），输入带故障的多变量时间序列，输出潜在表示 \( \mathbf{z}_i \in \mathbb{R}^{B_{\text{sub}} \times S \times d_{\text{model}}} \)。
  - 预训练头 \( P \)：多层感知机（MLP），将展平后的潜在表示映射回原始输入空间进行重构。
- **微调阶段**：冻结编码器参数，替换预训练头为新的MLP回归头（仅训练该头）。下游任务为估计车辆侧偏角（侧向速度）。

### 算法流程（文字说明）
1. 将批次 \( \mathbf{X} \) 按故障类型拆分为子批次。
2. 对每个子批次生成二进制掩码，并根据类型注入相应故障。
3. 所有子批次依次送入共享编码器，得到潜在表示。
4. 潜在表示经预训练头重建原始信号，计算掩码位置MSE。
5. 联合优化所有故障类型损失。

## 3. 实验设计

### 数据集与场景
- **主要数据集**：REVS Program Vehicle Database（2013年赛道采集，1963 Corvette Grand Sport），包含两段赛道数据（Monterey Motorsports Reunion 和 Targa Sixty-Six）。训练集用一段赛道，测试集包括同赛道和未见赛道（新赛道）两部分。
- **下游任务**：侧向速度（或侧偏角）估计，从11个传感器信号（如轮速、转向角、横摆角速度、加速度等）预测。
- **真实世界应用**：改装2019 Lexus LC 500在封闭赛道上进行闭环控制实验，用模型估计的侧偏角作为控制器反馈。

### 对比方法
- **非预训练基线**（non-pretrained baseline）：直接训练监督任务，无预训练。
- **均值掩码基线**（mean-only pretrained baseline）：仅使用Mean masking预训练（即传统置零掩码）。
- **本文方法**（Mean+Bias+Noise，简称MBN）。
- 额外对比：**SimMTM**（Dong et al. 2023，一种通用时间序列预训练方法）、**Kalman滤波**（基于物理模型）。

### 评估的故障模式
- **已见故障**：偏置（1σ偏移）、噪声（标准差0.4σ）、硬故障（置为均值）。
- **未见故障**：缩放错误（乘性因子2.0）。
- 附录中测试了完整故障分类（漂移、异常值、裁剪、时变缩放等）。

### 评估指标
- 侧向速度的均方误差（MSE），计算每个通道单独失效时的性能，并给出95%置信区间（bootstrap 200次）。

## 4. 资源与算力

- **训练硬件**：单张 NVIDIA H100 GPU。
- **预训练时长**：600 epochs，约3小时（每轮完整预训练+微调）。
- **微调时长**：50 epochs。
- **评估硬件**：Apple MacBook Pro (M3 Max, 128 GB RAM)，完整评估约20分钟。
- **总计**：项目历时数月进行超参数调优和架构探索，但每次实验均不超过单张H100。

## 5. 实验数量与充分性

- **主实验**：在REVS数据集上对4种故障模式（偏置、噪声、硬故障、缩放）分别评估，报告MSE（图4）。
- **消融实验**：
  - 不同掩码组合（7种组合，图7）。
  - 不同故障强度（图8-9）。
  - 10个随机种子（图10）。
  - 不同模型大小（32~512嵌入维度，图11）。
  - 预训练偏置范围/噪声比例的影响（图12-14）。
  - 多传感器同时失效（图15-16）。
  - 完整故障分类（漂移、异常值、裁剪等，图17）。
  - 与SimMTM对比（图18）。
  - 与Kalman滤波对比（表3，图19）。
  - 迁移至环境感知任务（北京PM10/PM2.5，图20-21）。
- **真实闭环控制实验**：在Lexus LC 500上分别测试轮速、横摆角速度、转向角、纵向速度传感器故障，记录轨迹和估计误差（图23-27）。
- **充分性与公平性**：
  - 实验覆盖了多种故障类型、强度、随机性、模型架构、任务领域，较为全面。
  - 对比方法包含学术基线（SimMTM）、物理模型基线（KF）以及简单掩码基线。
  - 所有实验均使用相同的数据划分和评估协议，消融实验设计系统。
  - 但真实实验仅在一个赛道场景（skidpad）上执行，且仅对比了非预训练基线，未与均值掩码基线对比。

## 6. 论文的主要结论与发现

1. **本文的多任务掩码预训练显著提升模型对传感器故障的鲁棒性**，在已见和未见故障上均优于非预训练基线和仅均值掩码基线。
2. **Bias掩码是关键组件**：缺少Bias掩码的模型对偏置和缩放故障的鲁棒性较差。
3. **泛化能力**：模型能泛化到预训练中未见的故障类型（如缩放错误），且跨赛道泛化良好。
4. **真实闭环控制验证**：在自动赛车场景中，本文方法在传感器故障下仍能安全行驶，而非预训练基线导致车辆偏离赛道。KF基线虽然优于非预训练模型，但不如本文方法。
5. **模型越大鲁棒性越好**：嵌入维度提升带来稳定的鲁棒性增益。
6. **迁移到其他领域**：在空气污染预测任务中同样提升鲁棒性。

## 7. 优点

- **针对性设计**：直接针对传感器故障模式设计掩码，而非通用随机掩码，更贴合实际需求。
- **简单有效**：不改变推理架构、不增加推理成本，仅修改预训练过程。
- **全面的鲁棒性评估**：包括多种故障类型、强度、组合、随机种子、模型大小、域迁移。
- **真实世界验证**：将模型部署到真实自动驾驶车辆并完成闭环控制实验，证明了方法的实用价值。
- **开源代码**：承诺公开代码，促进可复现性。

## 8. 不足与局限

- **所有故障模式权重相等**：未对不同传感器或故障类型赋予重要性权重，可能导致对关键故障的鲁棒性不足（如纵向速度故障仍困难）。
- **多任务梯度干扰**：同时优化多个掩码任务可能导致收敛不稳定，文中提及可尝试多任务学习技术（如梯度手术）但未实现。
- **实验覆盖有限**：仅在一个车辆数据集和一个真实平台（Lexus LC 500）上验证，更多领域（如机器人、航空）的泛化能力尚待证明。
- **仅评估了单传感器失效**：虽然附录有少量多传感器失效实验，但真实闭环实验仅针对单个传感器逐个注入故障。
- **纵向速度故障依然脆弱**：在闭环实验中，当纵向速度传感器失效时，本文方法同样导致不稳定，尽管比基线好。
- **没有比较其他鲁棒性方法**：如对抗训练、数据增强、域随机化等，缺乏与这些方法的直接对比（仅对比了掩码变体和SimMTM）。
- **Kalman滤波对比不完整**：KF利用物理模型和控制信号，与基于学习的方法并非完全同等的比较。

（完）
