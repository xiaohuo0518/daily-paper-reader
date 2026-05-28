---
title: Fourier Controller Networks for Real-Time Decision-Making in Embodied Learning
title_zh: 傅里叶控制器网络：面向具身学习的实时决策
authors: "Hengkai Tan, Songming Liu, Kai Ma, Chengyang Ying, Xingxing Zhang, Hang Su, Jun Zhu"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=nDps3Q8j2l"
tags: ["query:ur"]
score: 7.0
evidence: 使用傅里叶控制器网络实现低延迟实时决策
tldr: 本文提出傅里叶控制器网络（FCNet），通过短时傅里叶变换在频域提取时变特征并插值，解决了Transformer在机器人决策中数据效率低和推理延迟高的问题。FCNet在多个仿真和真实机器人任务上实现了实时性能，并显著降低了计算开销，非常适合边缘端部署。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-ndps3q8j2l/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 767, \"height\": 760, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-ndps3q8j2l/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1577, \"height\": 858, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-ndps3q8j2l/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 846, \"height\": 561, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-ndps3q8j2l/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 762, \"height\": 458, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-ndps3q8j2l/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 820, \"height\": 466, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-ndps3q8j2l/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1591, \"height\": 481, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-ndps3q8j2l/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 817, \"height\": 818, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-ndps3q8j2l/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1400, \"height\": 541, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-ndps3q8j2l/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1399, \"height\": 541, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-ndps3q8j2l/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1402, \"height\": 547, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-ndps3q8j2l/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1416, \"height\": 564, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-ndps3q8j2l/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1596, \"height\": 906, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-ndps3q8j2l/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1764, \"height\": 286, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-ndps3q8j2l/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1758, \"height\": 492, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-ndps3q8j2l/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1042, \"height\": 584, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-ndps3q8j2l/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1003, \"height\": 682, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-ndps3q8j2l/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 944, \"height\": 573, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-ndps3q8j2l/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 944, \"height\": 574, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-ndps3q8j2l/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 818, \"height\": 245, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-ndps3q8j2l/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1168, \"height\": 354, \"label\": \"Table\"}]"
motivation: Transformer在机器人决策中推理延迟高、数据效率低，难以满足实时需求。
method: 利用STFT将轨迹变换到频域，通过频域插值高效编码时变特征，并用轻量网络生成动作。
result: 在多个机器人控制任务上，FCNet保持高成功率，推理速度比Transformer快数倍。
conclusion: 频域方法为机器人实时决策提供新路径，适合边缘计算场景。
---

## Abstract
Transformer has shown promise in reinforcement learning to model time-varying features for obtaining generalized low-level robot policies on diverse robotics datasets in embodied learning. However, it still suffers from the issues of low data efficiency and high inference latency. In this paper, we propose to investigate the task from a new perspective of the frequency domain. We first observe that the energy density in the frequency domain of a robot's trajectory is mainly concentrated in the low-frequency part. Then, we present the Fourier Controller Network (FCNet), a new network that uses Short-Time Fourier Transform (STFT) to extract and encode time-varying features through frequency domain interpolation. In order to do real-time decision-making, we further adopt FFT and Sliding DFT methods in the model architecture to achieve parallel training and efficient recurrent inference. Extensive results in both simulated (e.g., D4RL) and real-world environments (e.g., robot locomotion) demonstrate FCNet's substantial efficiency and effectiveness over existing methods such as Transformer, e.g., FCNet outperforms Transformer on multi-environmental robotics datasets of all types of sizes (from 1.9M to 120M). The project page and code can be found https://thkkk.github.io/fcnet.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：现有在具身学习中广泛使用的 Transformer 架构虽然能够建模时变特征，但面临 **数据效率低**（需要大规模数据才能达到良好性能，而真实机器人数据收集成本高昂）和 **推理延迟高**（例如典型 Transformer 模型推理频率仅约 3Hz，但四足机器人控制要求 ≥ 50Hz）两大瓶颈，难以满足实时决策与边缘端部署需求。
- **研究动机**：作者从**频域**角度重新审视机器人轨迹，观察到自然界物理运动（如匀加速运动、简谐运动）以及真实机器人状态序列的**能量密度主要集中于低频部分**，高频多属于传感器噪声。这一现象启发了作者利用频域压缩与插值进行高效建模，从而降低计算复杂度、提升数据效率。
- **整体含义**：本文旨在为具身学习提供一种新的神经网络架构——傅里叶控制器网络（FCNet），通过引入频域归纳偏置，在保证高性能的同时大幅降低训练与推理的时间复杂度，使得实时机器人控制成为可能。

## 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

### 核心思想
- 基于“机器人轨迹能量集中在低频”的观察，将历史状态窗口通过 **短时傅里叶变换（STFT）** 转换到频域，仅保留最低的 **m** 个频率模式（m ≪ n，n 为窗口长度），在频域进行线性变换后逆变换回时域，从而滤除高频噪声并提取核心运动特征。
- 利用 **FFT 卷积** 实现并行训练，利用 **滑动 DFT** 实现递归式单步推理，使推理复杂度降至 O(m)（与上下文长度 n 无关）。

### 关键技术细节

1. **整体架构**  
   - 输入：历史状态窗口 \(X_0 \in \mathbb{R}^{n \times d_s}\)  
   - 位置编码器 \(P\)（单层 FFN）将维度映射到隐藏维度 \(d_h\)  
   - L 个堆叠的傅里叶层，每个傅里叶层包含：
     - **因果谱卷积（CSC）块**：在频域建模时序依赖
     - **位置逐点 FFN 块**：在隐藏维度上建模特征
   - 位置解码器 \(Q\)（两层 FFN）输出预测动作序列 \(X_{L+2} \in \mathbb{R}^{n \times d_a}\)

2. **因果谱卷积（CSC）块**  
   - 对每个步长 \(t\)，仅基于历史输入 \(x_0, ..., x_t\) 计算输出 \(y_t\)，保证因果性。  
   - 对输入序列 \(X\) 做 DFT，保留 **m** 个低频模式 \(\hat{X} \in \mathbb{C}^{m \times d_h}\)。  
   - 在频域应用可学习的线性权重矩阵 \(W \in \mathbb{C}^{m \times m}\) 得到 \(\hat{Y}\)。  
   - 通过共轭对称扩展（公式 (6)）得到全频域 \(\hat{Z} \in \mathbb{C}^{n \times d_h}\)，再经 IDFT 取出最后一个时域值 \(y_{n-1}\)（即当前步输出）。  
   - 数学表达：见公式 (5)~(7)。

3. **并行训练**  
   - 利用递归形式 \(\hat{X}^{(t)} = u \odot (\hat{X}^{(t-1)} + x_t - x_{t-n})\)（公式 (9)）可转换为 FFT 卷积形式，从而一次性计算所有 \(t=0...n-1\) 的 \(\hat{X}^{(t)}\)，复杂度为 \(O(m d_h n \log n)\)。  
   - 再加频域线性变换 \(W \hat{X}\) 的 \(O(m^2 d_h n)\)，训练总复杂度为 \(O(m n \log n + m^2 n)\)。

4. **高效递归推理**  
   - 缓存上一时刻的 \(\hat{X}'\)，新输入 \(x_{n-1}\) 时通过滑动 DFT 更新：\(\hat{x}_k = e^{j2\pi k/n}(\hat{x}'_k - x_{-1} + x_{n-1})\)（公式 (13)），复杂度 \(O(m)\)。  
   - 频域变换和逆变换的预处理使推理总复杂度为 \(O(m d_h + d_h^2)\)，简化为 \(O(m)\)。

### 算法流程（文字说明）
1. 给定当前窗口 \(X_0\)（历史 n 个状态）。
2. 位置编码器 \(P\) 映射到隐藏空间，得到 \(X_1\)。
3. 经过 L 个傅里叶层，每个层内：
   - 先 LayerNorm，再 CSC 块提取频域特征，加残差。
   - 再 LayerNorm，再 FFN 块，加残差。
4. 位置解码器 \(Q\) 输出预测动作 \(X_{L+2}\)。
5. 训练时使用 MSE 或 KL 散度损失（公式 (4)）进行监督学习（可结合 return-to-go 实现离线 RL）。

## 3. 实验设计：使用的数据集/场景、benchmark、对比方法

### 数据集与场景
- **D4RL MuJoCo**（离线 RL 标准基准）：HalfCheetah、Walker2d、Hopper 的 medium-expert、medium、medium-replay 三个难度等级，共 9 个任务。
- **D4RL Adroit**（机器人灵巧操作）：pen、hammer、door、relocate 的 human、cloned、expert 共 12 个任务。
- **多环境四足机器人数据集**（自建）：在 IsaacGym 中模拟 Unitree Aliengo 机器人，包含 6 种技能（站立、奔跑、爬行、挤压、倾斜、跑步）和 5 种地形（粗糙地形、楼梯、斜坡、障碍物等），共 32 万条轨迹、6000 万步（60M）。使用专家级 RL 策略采集。
- **真实机器人部署**：将训练好的 FCNet 零样本迁移到真实 Unitree Aliengo 机器人，测试室内楼梯、草地、雪地、冰面等未见地形。

### Benchmark 与对比方法
- D4RL MuJoCo：对比 **MLP 类**（BC、CQL、BEAR、BRAC-v、AWR）、**Transformer 类**（DT）、**RetNet 类**（DT-RetNet，将 DT 的 Transformer 替换为 RetNet）。
- D4RL Adroit：对比 DT、BC、CQL。
- 多环境四足机器人：主要对比 Transformer（参数数量相近），以及展示了不同数据集规模（1.9M~120M）下 FCNet 与 Transformer 的性能曲线。
- 推理延迟：对比 Transformer（带 KV cache）在不同上下文长度、层数、隐藏大小下的 CPU 推理延迟。

## 4. 资源与算力
- 论文**未明确说明**训练所使用的 GPU 型号、数量及具体训练时长。仅在附录 C.4 中提到推理延迟测试环境为 Intel(R) Xeon(R) Silver 4210 CPU @ 2.20GHz，未提及 GPU。
- 根据实验规模（D4RL 每个任务 3-5 个种子，多环境数据集 1500 条轨迹评估），推测使用了中等规模的 GPU（如 V100 或 A100），但原文未披露具体细节。这是论文的一个信息缺失点。

## 5. 实验数量与充分性

### 实验数量
- D4RL MuJoCo：9 个任务 × 3 个随机种子，报告均值和方差。对比 8 种方法。
- D4RL Adroit：12 个任务 × 5 个随机种子，对比 3 种方法。
- 多环境四足机器人：不同数据集规模（1.9M~120M 共 7 个点），以及不同模型参数（层数 2/4/8，隐藏大小变化）、不同上下文长度（32~160）的性能与延迟。每个点至少 1500×3 条轨迹。
- 推理延迟：3 个随机种子 × 10 轮，取平均。涵盖三个变量（上下文长度、层数、隐藏大小）的扫描。
- 真实机器人：定性的视频演示，无定量指标。
- 消融实验（附录 B）：不同层数、隐藏大小、上下文长度下的性能对比，以及参数数量-性能-延迟的联合分析。

### 充分性与公平性评价
- **充分性较高**：从标准离线 RL 基准到自建大规模数据集，再到真实机器人，覆盖了仿真与真实场景；对比方法全面（包括 MLP、Transformer、SSM）；消融实验考虑了架构超参数和模型规模的影响。
- **公平性**：在多环境四足机器人实验中将 FCNet 与 Transformer 的参数数量保持大致相等（约 790k），学习率、优化器等超参数分别调优。在推理延迟测试中统一使用 CPU 进行公平对比。
- **潜在偏差**：真实机器人实验仅展示定性结果，缺乏定量指标（如成功率、步态幅度等）；未与最新的 SSM（如 Mamba）对比（仅对比了 RetNet，且仅在 D4RL 中）；D4RL 实验的 FCNet 超参数（如 m=10，n=64）是固定的，未说明是否对每个任务做了独立调优，可能影响最优性。

## 6. 论文的主要结论与发现

1. **频域归纳偏置有效**：机器人轨迹的能量集中在低频，利用低频模式建模（m ≪ n）可以高精度提取时变特征，同时滤除噪声。
2. **FCNet 性能大幅超越 Transformer**：
   - D4RL MuJoCo 平均得分 FCNet (75.1) > DT (74.7) > DT-RetNet (63.6) > 其他方法。
   - D4RL Adroit 平均得分 FCNet (41.0) > DT (27.8)，在 9/12 任务上领先。
   - 多环境四足机器人数据集上，FCNet 在所有规模（1.9M~120M）下均优于 Transformer，尤其在数据量小时优势更显著（Transformer 几乎失效）。
3. **推理效率极高**：FCNet 的 CPU 推理延迟始终低于 Transformer，随上下文长度增加几乎不变（~2ms），而 Transformer 线性增长至 7ms+；随层数和隐藏大小增加，FCNet 延迟增长缓慢，始终 <20ms，满足实时控制要求。
4. **可迁移至真实世界**：零样本部署在真实四足机器人上能够流畅行走于多种未见地形，而 Transformer 因延迟高、输出不平滑导致摔倒或表现欠佳。

## 7. 优点

- **创新性**：首个系统性地将频域分析引入具身学习序列建模，利用机器人运动的物理先验（低频主导）设计高效架构。
- **效率与性能兼顾**：训练复杂度 O(mn log n + m²n)，推理复杂度 O(m)，远低于 Transformer 的 O(n²) 训练和 O(n) 推理；同时性能不降反升，尤其在数据有限时。
- **实验严谨**：覆盖多种基准（离线 RL、四足控制、真实机器人）；对比方法包括主流架构；消融实验全面（参数、长度、层数）。
- **实用性强**：设计支持并行训练和递归推理，易于在边缘端（CPU）部署，延迟低至 2ms，满足机器人实时控制要求。
- **开放性好**：提供了项目页面和代码，部分数据集公开，便于复现与推广。

## 8. 不足与局限

- **未验证大规模可扩展性**：本文仅使用自建 60M 步数据集，未在更大规模（如 RT-1 的 130k 条轨迹）或跨模态数据（视觉、语言）上训练，尚不确定 FCNet 是否能像 Transformer 一样通过扩大数据规模持续提升。
- **高频信息可能丢失**：FCNet 主动过滤了高频成分，但某些场景（如快速冲击、碰撞、精细操作）可能需要高频信息，论文未考虑这类情况。
- **缺乏在线 RL 验证**：当前仅在离线模仿学习和离线 RL 设定下评估，未在在线强化学习或交互式训练中测试 FCNet 的适应性和收敛性。
- **与最新 SSM 对比不充分**：仅对比了 RetNet，未与 Mamba、Hyena 等更新模型对比；且在 D4RL 上 RetNet 实现可能不是最优，导致结论偏向 FCNet。
- **真实机器人实验定量缺失**：仅提供视频，没有量化数据（如运动速度、成功率、能量消耗等），降低了说服力。
- **算力信息不透明**：未报告 GPU 型号、训练时间等，难以判断训练成本。
- **超参数选择依赖经验**：模式数 m 由经验公式 min{2.5 log n, floor(n/2)+1} 决定，未提供自适应或自动选择方法，可能在不同任务上需要手动调整。

（完）
