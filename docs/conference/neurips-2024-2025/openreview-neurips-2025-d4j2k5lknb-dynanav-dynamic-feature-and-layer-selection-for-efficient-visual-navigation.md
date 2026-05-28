---
title: "DynaNav: Dynamic Feature and Layer Selection for Efficient Visual Navigation"
title_zh: DynaNav：面向高效视觉导航的动态特征与层选择
authors: "Jiahui Wang, Changhao Chen"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=D4j2K5lknb"
tags: ["query:ur"]
score: 8.0
evidence: 面向边缘设备的动态特征与层选择以提升视觉导航效率
tldr: 视觉导航模型在边缘设备上部署受限于高计算开销。本文提出DynaNav，通过可训练硬特征选择器与早退机制，根据场景复杂度动态调整特征和层，在保持导航性能的同时大幅降低计算成本，经贝叶斯优化确定退出阈值，适用于资源受限的机器人平台。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4j2k5lknb/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1427, \"height\": 580, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4j2k5lknb/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 738, \"height\": 574, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4j2k5lknb/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 872, \"height\": 526, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4j2k5lknb/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 794, \"height\": 379, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4j2k5lknb/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 867, \"height\": 341, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4j2k5lknb/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1430, \"height\": 312, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4j2k5lknb/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1196, \"height\": 1794, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4j2k5lknb/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1103, \"height\": 1654, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4j2k5lknb/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1102, \"height\": 1652, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4j2k5lknb/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1103, \"height\": 1652, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4j2k5lknb/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1450, \"height\": 466, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4j2k5lknb/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1445, \"height\": 275, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4j2k5lknb/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 802, \"height\": 431, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4j2k5lknb/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 876, \"height\": 206, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4j2k5lknb/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 880, \"height\": 1531, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4j2k5lknb/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1172, \"height\": 565, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4j2k5lknb/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1092, \"height\": 433, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4j2k5lknb/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1264, \"height\": 371, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4j2k5lknb/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1096, \"height\": 262, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4j2k5lknb/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1455, \"height\": 206, \"label\": \"Table\"}]"
motivation: 现有视觉导航基础模型计算开销大且可解释性差，限制了边缘设备部署。
method: 提出动态特征和层选择框架，结合可训练硬选择器和早退机制，由贝叶斯优化确定退出阈值。
result: 在真实世界数据集和仿真环境中，DynaNav显著降低计算量且性能接近基准。
conclusion: 动态选择机制能有效实现边缘设备上的高效视觉导航。
---

## Abstract
Visual navigation is essential for robotics and embodied AI. However, existing foundation models, particularly those with transformer decoders, suffer from high computational overhead and lack interpretability, limiting their deployment on edge devices. To address this, we propose DynaNav, a Dynamic Visual Navigation framework that adapts feature and layer selection based on scene complexity. It employs a trainable hard feature selector for sparse operations, enhancing efficiency and interpretability. Additionally, we integrate feature selection into an early-exit mechanism, with Bayesian Optimization determining optimal exit thresholds to reduce computational cost. Extensive experiments in real-world-based datasets and simulated environments demonstrate the effectiveness of DynaNav. Compared to ViNT, DynaNav achieves a $2.6\times$ reduction in FLOPs, 42.3% lower inference time, and 32.8% lower memory usage while improving navigation performance across four public datasets.

---

## 论文详细总结（自动生成）

# 论文总结：DynaNav: Dynamic Feature and Layer Selection for Efficient Visual Navigation

## 1. 核心问题与整体含义（研究动机和背景）
- **背景**：视觉导航是机器人和具身智能的基础能力，现有基础模型（如 ViNT、NoMaD）基于 Transformer 解码器，在大规模训练中表现优异，但存在**计算开销大**、**可解释性差**的问题，尤其不利于在资源受限的边缘设备（如机器人）上部署。
- **核心问题**：是否需要在所有导航场景中激活所有 Transformer 层？哪些特征对解码最重要？能否识别关键区域（像素）并动态跳过冗余计算？
- **整体目标**：受人类大脑根据任务复杂度动态调用神经元的启发，提出一种**动态视觉导航框架 DynaNav**，根据场景复杂度自适应选择特征和层，在保持或提升导航性能的同时大幅降低计算成本。

## 2. 方法论
### 2.1 核心思想
- 结合**动态特征选择**（可训练硬选择器产生稀疏表示）与**早退机制**（基于中间层输出一致性的早期退出），并利用**贝叶斯优化**确定最优退出阈值。
- 仅在简单场景使用少数特征和层，复杂场景则调动更多资源。

### 2.2 关键技术细节
1. **特征提取**：使用 EfficientNet-B0 编码器处理观测图像序列（`o_{t-p:t}`）和早期融合的目标图像（`[ot; os]`）。
2. **动态特征选择器**（图 2）：
   - 对编码后的特征通过 MLP 投影到更高维，再对每个像素执行 **Gumbel-Softmax** 操作，生成二值 mask（保留/丢弃）。
   - mask 与特征逐元素相乘实现稀疏化，减少后续 Transformer 计算量，同时提升可解释性（通过可视化 saliency map 显示哪些区域被选中）。
3. **Transformer 解码器**：
   - 堆叠的多头自注意力层（4 层）处理稀疏化后的视觉 tokens。
   - 训练时引入**随机早退触发**（在第 1、2、3 层后随机计算中间预测），使模型学会在任意层产生可用输出。
4. **早退判定（推理阶段）**：
   - 使用**动作一致性条件**：如果当前层的预测 `h(x_i)` 与上一层的预测 `h(x_{i-1})` 的 L2 距离小于阈值 `η_i`，则退出；同时，若目标与当前观测差异极小（基于被掩膜像素数），甚至可在解码器前直接退出。
   - 阈值 `η` 通过**贝叶斯优化**（结合 FLOPs、推理时间、GPU 内存约束）从验证集上搜索获得。
5. **预测头**：4 层 Transformer + 单隐层 MLP 输出动作 `a_t` 和航点偏移 `w_t`。

### 2.3 训练与优化
- 损失函数：最大化动作和航点与真值的似然，含超参数 λ（论文取 0.5）。
- 贝叶斯优化的目标：最大化预测与真值的余弦相似度，同时惩罚违反约束（FLOPs ≤ Fmax, Time ≤ Tmax, Memory ≤ Gmax）的阈值组合。

## 3. 实验设计
### 3.1 数据集与场景
- **真实世界基准**（4 个公开数据集）：
  - **Recon**：室外中速（~2m/s）
  - **SCAND**：中等速度，含环境交互
  - **Go-Stanford**：低速室内（~0.5m/s）
  - **SACSoN**：中速室内
  - 每个数据集随机 80% 训练 / 20% 测试。
- **CARLA 仿真环境**：3 个场景（Town02 简单、Town03 中等、Town10 困难），各 20 条轨迹，速度 20 km/h。使用 BehaviorAgent 驾驶，数据频率 4Hz。

### 3.2 对比方法与评估指标
- 对比方法：**ViNT**（主要基线）、**NoMaD**（扩散策略）、**GNM**（轻量模型）。
- 评估指标：
  - 导航性能：动作余弦相似度 `Sim(at, agt)` 和航点余弦相似度 `Sim(wt, wgt)`（百分比），以及损失值 `L_action`, `L_dist`。
  - 效率指标：**FLOPs**（×10⁹）、**推理时间**（秒/轨迹）、**GPU 内存**（GB）。
  - CARLA 中额外报告**成功率**（进度长度/总长度）。

## 4. 资源与算力
- 论文中**未明确说明 GPU 型号、数量或总训练时长**。
- 仅在附录给出了超参数：
  - 训练 100 epoch + 微调 80 epoch
  - 输入图像 85×64，批大小 256
  - 优化器 AdamW，余弦退火学习率 5e-4（微调时 1e-4）
  - 编码器 EfficientNet-B0，隐藏维度 1280
  - 解码器 4 层，4 注意力头
  - 未提及具体 GPU 类型（可能为单卡或少量 GPU，需猜测）。

## 5. 实验数量与充分性
- **大量实验**：在 4 个真实数据集、CARLA 的 3 个场景上进行对比；消融实验涵盖：
  - 模块有效性（动态解码器、特征选择器组合 vs 固定一半层/通道）
  - 阈值优化方法（有无贝叶斯优化、是否允许解码器前退出）
  - 特征选择对早退的贡献（跳层频率、选择特征数与跳层关系）
  - 约束消融（移除 FLOPs/时间/内存约束）
  - 鲁棒性（每个轨迹重复 10 次）
  - 时间片段一致性（700 帧分段分析）
  - Mamba 解码器替代
  - 目标视角变化鲁棒性（不同角度/位置）
- **充分性判断**：实验覆盖面广，对比公平（与 ViNT、NoMaD 相同训练设置），消融设计严谨，控制变量充分。但缺少在真实机器人上的部署验证，存在 sim2real 局限。

## 6. 主要结论与发现
- **DynaNav 在 4 个基准上平均节省约 58% FLOPs**（4.37×10⁹→1.86×10⁹），推理时间降低 42.3%，内存降低 32.8%。
- **导航性能不降反升**：动作相似度提升 0.83%，航点相似度提升 0.28%（相比 ViNT）。
- CARLA 中成功率与 ViNT 持平（~0.73/0.66/0.59），但 FLOPs 仅其一半（1.58/1.70/1.93 vs 4.37）。
- 场景越复杂（室内→室外），模型自动激活更多层，验证动态假设。
- 特征选择器产生的 saliency map 表明：模型关注的不总是最大共同物体，而是**导航方向上的空间信息**，增强可解释性。

## 7. 优点
- **创新性**：首次将动态网络（早退+特征选择）引入端到端视觉导航，解决计算效率与可解释性双重挑战。
- **方法设计精巧**：Gumbel-Softmax 的可训练硬选择器可实现精确稀疏化，且与早退机制协同（稳定跳层频率）；贝叶斯优化自动权衡性能与约束，无需手动调参。
- **实验充分**：包含多种环境、多种对比、多角度消融，结果具有统计意义。
- **可解释性贡献**：通过可视化选中的像素区域，揭示模型决策依据，有助于后续调试与安全审查。

## 8. 不足与局限
- **需要额外优化过程**：贝叶斯优化在训练后执行，增加了开发/部署劳动成本，尚未实现端到端联合优化。
- **早退可能损失精度**：允许解码器前直接退出时，性能略有下降（Sim 下降约 0.1%），需谨慎选择是否启用。
- **场景覆盖有限**：仅在仿真 CARLA 中验证成功率，未在真实机器人平台上测试；sim2real 差距是潜在风险。
- **计算资源未公开**：无法重复或评估硬件要求；训练时使用图像分辨率偏低（85×64），真实场景可能需更高分辨率。
- **鲁棒性测试规模小**：CARLA 仅 20 条轨迹，每条重复 10 次，暂时不足以保证统计显著性；真实世界测试缺乏。
- **对比方法较少**：未与更多现代轻量化模型（如纯卷积、SSM-based）在同等条件下对比；仅对比了 Mamba，但 Mamba 在短序列不占优。

（完）
