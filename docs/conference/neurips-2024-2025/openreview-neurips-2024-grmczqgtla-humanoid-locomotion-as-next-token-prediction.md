---
title: Humanoid Locomotion as Next Token Prediction
title_zh: 人形机器人行走作为下一词元预测
authors: "Ilija Radosavovic, Bike Zhang, Baifeng Shi, Jathushan Rajasegaran, Sarthak Kamat, Trevor Darrell, Koushil Sreenath, Jitendra Malik"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=GrMczQGTlA"
tags: ["query:ur"]
score: 6.0
evidence: 利用多种数据源构建人形机器人运动序列数据集
tldr: 该论文将人形机器人行走控制建模为下一词元预测问题，利用因果Transformer自动回归预测传感器运动序列。模型在包含先前策略、模型控制器、动作捕捉及YouTube人类视频的多模态数据集上训练，实现了零样本的真实世界行走。尽管重点在于运动控制而非数据集构建，但其多源数据融合方法为人形机器人数据集构建提供了参考。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-grmczqgtla/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1423, \"height\": 1564, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-grmczqgtla/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1401, \"height\": 435, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-grmczqgtla/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1275, \"height\": 391, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-grmczqgtla/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1434, \"height\": 381, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-grmczqgtla/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1407, \"height\": 367, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-grmczqgtla/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1369, \"height\": 439, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-grmczqgtla/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 608, \"height\": 426, \"label\": \"Figure\"}]"
motivation: 现有方法难以利用多模态、缺失模态的数据进行人形机器人控制。
method: 提出因果Transformer，按模态对齐方式自动回归预测传感器运动序列。
result: 模型在真实人形机器人上实现零样本行走，并能迁移到真实世界。
conclusion: 将人形控制视为序列预测任务可有效利用多样化数据。
---

## Abstract
We cast real-world humanoid control as a next token prediction problem, akin to predicting the next word in language. Our model is a causal transformer trained via autoregressive prediction of sensorimotor sequences. To account for the multi-modal nature of the data, we perform prediction in a modality-aligned way, and for each input token predict the next token from the same modality. This general formulation enables us to leverage data with missing modalities, such as videos without actions. We train our model on a dataset of sequences from a prior neural network policy, a model-based controller, motion capture, and YouTube videos of humans. We show that our model enables a real humanoid robot to walk in San Francisco zero-shot. Our model can transfer to the real world even when trained on only 27 hours of walking data, and can generalize to commands not seen during training. These findings suggest a promising path toward learning challenging real-world control tasks by generative modeling of sensorimotor sequences.

---

## 论文详细总结（自动生成）

# 人形机器人行走作为下一词元预测——论文详细总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：近年来，大型语言模型通过对海量互联网文本进行下一词元预测，获得了强大的表征与泛化能力。本文试图将这一范式推广到机器人领域，探索是否可以通过对传感器-运动序列（sensorimotor sequences）的自回归生成建模，学习到有效的机器人控制模型。
- **核心问题**：人形机器人行走控制是一个高维、多模态的挑战性任务。现有方法主要依赖强化学习或模型预测控制，但难以利用多种来源（如人类视频、动作捕捉）的异构数据。本文提出将人形机器人控制视为“下一词元预测”问题，使得模型能够从包含缺失模态（如无动作标签的视频）的数据中学习。
- **整体含义**：通过统一框架，将自然语言处理中的生成式预训练思路迁移到具身智能，为机器人学习提供了一种可扩展、数据兼容的新路径。

## 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

### 核心思想
- 将传感器运动轨迹视作“物理世界的句子”，采用因果Transformer进行自回归预测。目标是建模完整的联合概率分布 \( p(t) = \prod p(t_k | t_{k-1}, \dots, t_1) \)，其中每个 token 包含观察（o）和动作（a）。

### 关键技术细节
1. **Token化与嵌入**：将每个时间步的观察向量 \( o_i \in \mathbb{R}^m \) 和动作向量 \( a_i \in \mathbb{R}^n \) 拼接，通过线性投影层映射为 d 维嵌入。
2. **模态对齐预测（Modality-aligned prediction）**：与语言模型中预测下一个 token 不同，本文对于每个输入 token，预测同模态的下一个 token（即从当前观察预测下一观察，从当前动作预测下一动作）。这允许模型处理部分缺失的模态。
3. **缺失模态处理**：当动作或某些观察缺失时，使用可学习的 mask token [M] 填充，在训练时忽略对应位置的损失。这样可以将无动作的轨迹（如人类视频、运动捕捉）转化为完整格式参与训练。
4. **联合训练**：可以同时对完整轨迹和带掩码的轨迹进行联合训练，或先预训练后微调。实验表明两者效果相当，默认采用联合训练。
5. **模型架构**：标准因果Transformer，包含 LayerNorm、多头自注意力（因果掩码）、MLP。隐藏维度192，4层，4头注意力，上下文窗口为16个时间步（可扩展）。
6. **推理过程**：在真实机器人上，模型以自回归方式运行：输入当前观察和动作，预测下一观察和动作；仅执行预测的动作，丢弃预测的观察，并用真实观察更新输入。

### 公式/算法流程（文字说明）
- 训练目标：最小化负对数似然 \( \mathcal{L} = \sum_{t \in D} -\log p(t) \)，假设预测分布为固定方差的高斯分布。
- 前向过程：输入序列 \( \{h^0_1, h^0_2, \dots\} \)，经过 L 层 Transformer 得到 \( h^L_i \)，再通过线性投影得到预测的 \( \hat{o}_{i+1}, \hat{a}_{i+1} \)。

## 3. 实验设计：数据集、场景、benchmark、对比方法

### 数据集
论文构建了一个多样化的轨迹数据集，来源包括：
- **神经网络策略轨迹**（10k条，每段10秒）：来自先前用强化学习训练的策略 [29]，包含完整观察和动作。
- **模型控制器轨迹**（20k条，每段10秒）：来自Agility Robotics的模型控制器，仅记录观察，无动作。
- **人类运动捕捉轨迹**（约1k条站立/行走轨迹）：来自KIT数据集（AMASS），通过逆运动学重定向到机器人形态。
- **YouTube人类视频轨迹**：使用PHALP提取3D人体姿态，再重定向到机器人，经过筛选保留低误差轨迹。

### 场景与评估
- **真实世界部署**：在旧金山多个地点（人行道、沥青、瓷砖广场、沙土路等）测试机器人行走，持续一周。
- **仿真评估**：使用MuJoCo仿真器，机器人从静止开始，给定恒定的前进速度（0.35 - 0.70 m/s）和偏航角速度（-0.4 - 0.4 rad/s）。
- **主要指标**：
  - **位置跟踪误差**：机器人实际轨迹与理想轨迹之间的平均距离。
  - **预测误差**：在验证集上的下一词元预测损失（观察+动作）。

### 对比方法
- 主要对比基线为**大规模强化学习方法** [29]（即生成训练数据的RL策略）。论文展示了在轨迹跟踪精度上的优势。
- 此外，还进行了消融实验：训练数据量、上下文长度、模型大小的影响，以及是否包含无动作数据。

## 4. 资源与算力
- 论文明确提到训练在 **4块 NVIDIA A100 GPU** 上进行。
- 未说明具体训练时长，但提到模型规模从1M到8M参数，数据集总轨迹数约3万条（10k+20k+1k+视频），训练时间应在数小时量级。

## 5. 实验数量与充分性
- **实验组数**：包含多组消融实验：
  - 与RL基线对比（图5、图6左）
  - 使用无动作数据的效果（图6右）
  - 数据规模缩放（图7左）
  - 上下文长度影响（图7中）
  - 模型大小影响（图7右）
  - 预测误差与跟踪误差相关性分析（图8，14个模型）
- **充分性与公平性**：
  - 实验中随机采样命令、多次重复（N=245），有统计意义。
  - 对比方法采用相同机器人平台和仿真环境，公平。
  - 真实世界测试虽未提供定量指标，但视频展示了多种地形下的表现，增加了说服力。
  - 消融实验系统，覆盖了数据、架构、训练目标等关键方面。
- **不足之处**：缺少与模型控制器（MPC）的直接定量对比；真实世界无定量跟踪误差数据；未对比其他生成式控制方法（如扩散策略）。

## 6. 论文的主要结论与发现
1. **序列生成可实现有效控制**：仅通过自回归预测传感器运动序列，就能在真实人形机器人上实现零样本行走，且跟踪精度优于产生训练数据的RL策略。
2. **缺失模态数据有益**：即使没有动作标签，无动作的轨迹（模型控制器、运动捕捉、人类视频）也能提升模型性能。
3. **良好的缩放特性**：模型性能随数据量、上下文窗口大小、模型参数量的增加而提升。
4. **预测误差与任务性能高度相关**：Pearson系数 r=0.87，说明预测损失可作为无需仿真的评价指标。
5. **泛化能力**：模型能够泛化到训练中未见的命令（如不同偏航速度），并适应旧金山的真实环境。

## 7. 优点：方法或实验设计上的亮点
- **统一框架**：将不同来源（仿真、人类数据）的异构数据统一到同一自回归建模框架中，无需复杂的数据对齐。
- **模态对齐预测**：新颖地处理了多模态数据，使模型能处理部分缺失信息，这是语言建模中不常见的挑战。
- **零样本真实世界迁移**：仅在仿真数据上训练（含部分真实人类数据），直接部署到真实机器人，无需域随机化或微调。
- **丰富的消融实验**：系统验证了数据、模型、上下文等缩放特性，并发现了预测误差与性能的相关性，有助于未来节省仿真评估成本。
- **开源友好的表述**：详细描述了数据集构建过程（逆运动学重定向、过滤器等），可复现性较好。

## 8. 不足与局限
- **鲁棒性不足**：论文承认模型仍落后于最先进的MPC控制器，且在鲁棒性方面弱于RL基线（未详细量化）。
- **数据依赖问题**：YouTube视频数据的处理依赖计算机视觉技术（PHALP），在实际中需要大量人工筛选，限制了大规模扩展。
- **仿真与真实鸿沟**：虽然实现了零样本，但仿真评估仅基于MuJoCo，真实世界的性能尚未与模型控制器进行严格对比（例如摔倒率、扰动恢复能力）。
- **缺乏跨任务泛化评估**：仅测试了行走（直行和转弯），未评估跳跃、上下坡、避障等复杂动作。
- **超参数选择说明不足**：模型默认超参数（隐藏尺寸192、4层等）如何确定未说明，可能缺乏充分调优。
- **统计误差未报告**：图中未显示误差条或置信区间，实验结果的统计显著性不够明确。

（完）
