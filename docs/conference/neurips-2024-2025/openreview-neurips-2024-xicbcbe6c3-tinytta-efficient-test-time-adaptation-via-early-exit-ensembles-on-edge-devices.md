---
title: "TinyTTA: Efficient Test-time Adaptation via Early-exit Ensembles on Edge Devices"
title_zh: TinyTTA：通过早期退出集成实现边缘设备上的高效测试时适应
authors: "Hong Jia, Young D. Kwon, Alessio Orsino, Ting Dang, Domenico Talia, Cecilia Mascolo"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=XIcBCBe6C3"
tags: ["query:ur"]
score: 9.0
evidence: 在资源受限的边缘设备上进行测试时适应
tldr: 该论文提出TinyTTA，一种基于早期退出集成的测试时适应方法，专为微控制器等边缘设备设计。TinyTTA通过多个提前退出分支的集成来适应数据分布变化，同时保持低计算和存储开销。实验表明，该方法在资源受限的机器人应用中能有效提升模型鲁棒性，为人形机器人边缘部署提供了实用方案。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-xicbcbe6c3/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1437, \"height\": 376, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xicbcbe6c3/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1445, \"height\": 331, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xicbcbe6c3/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1446, \"height\": 467, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xicbcbe6c3/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1449, \"height\": 262, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xicbcbe6c3/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1441, \"height\": 392, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xicbcbe6c3/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1466, \"height\": 590, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xicbcbe6c3/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 584, \"height\": 395, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xicbcbe6c3/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1434, \"height\": 320, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xicbcbe6c3/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1448, \"height\": 307, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xicbcbe6c3/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1457, \"height\": 690, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xicbcbe6c3/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 575, \"height\": 338, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xicbcbe6c3/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 507, \"height\": 404, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xicbcbe6c3/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1446, \"height\": 304, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xicbcbe6c3/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1416, \"height\": 334, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xicbcbe6c3/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1420, \"height\": 336, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-xicbcbe6c3/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 659, \"height\": 279, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xicbcbe6c3/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 880, \"height\": 143, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xicbcbe6c3/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1456, \"height\": 550, \"label\": \"Table\"}]"
motivation: 边缘设备资源受限，难以进行连续模型适应以应对数据分布偏移。
method: 提出多分支早期退出网络，在推理时集成不同深度的预测以高效适应分布变化。
result: 在微控制器上实现低开销的测试时适应，性能优于其他方法。
conclusion: TinyTTA使边缘机器人能够在线适应环境变化，提升可靠性。
---

## Abstract
The increased adoption of Internet of Things (IoT) devices has led to the generation of large data streams with applications in healthcare, sustainability, and robotics. In some cases, deep neural networks have been deployed directly on these resource-constrained units to limit communication overhead, increase efficiency and privacy, and enable real-time applications. However, a common challenge in this setting is the continuous adaptation of models necessary to accommodate changing environments, i.e., data distribution shifts. Test-time adaptation (TTA) has emerged as one potential solution, but its validity has yet to be explored in resource-constrained hardware settings, such as those involving microcontroller units (MCUs). TTA on constrained devices generally suffers from i) memory overhead due to the full backpropagation of a large pre-trained network, ii) lack of support for normalization layers on MCUs, and iii) either memory exhaustion with large batch sizes required for updating or poor performance with small batch sizes. In this paper, we propose TinyTTA, to enable, for the first time, efficient TTA on constrained devices with limited memory. To address the limited memory constraints, we introduce a novel self-ensemble and batch-agnostic early-exit strategy for TTA, which enables continuous adaptation with small batch sizes for reduced memory usage, handles distribution shifts, and improves latency efficiency. Moreover, we develop the TinyTTA Engine, a first-of-its-kind MCU library that enables on-device TTA. We validate TinyTTA on a Raspberry Pi Zero 2W and an STM32H747 MCU. Experimental results demonstrate that TinyTTA improves TTA accuracy by up to 57.6\%, reduces memory usage by up to six times, and achieves faster and more energy-efficient TTA. Notably, TinyTTA is the only framework able to run TTA on MCU STM32H747 with a 512 KB memory constraint while maintaining high performance.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 一、核心问题与整体含义（研究动机和背景）

- **核心问题**：边缘设备（如微控制器 MCU）资源严重受限（例如 STM32H747 仅有 512 KB SRAM），传统测试时适应（TTA）方法因全网络反传播内存开销大、不支持归一化层、依赖大 batch 尺寸等原因，无法直接部署。
- **研究背景**：IoT 设备产生大量数据流，需要模型持续适应环境变化（如传感器噪声、天气变化等数据分布偏移）。现有 TTA 方法（如 TENT、CoTTA、EATA）在 GPU 上有效，但在 MCU 上内存不足。
- **整体含义**：本文首次提出能在 MCU 上高效运行的 TTA 框架 TinyTTA，通过早退（early-exit）集成和权重标准化（WS）克服资源限制，使资源受限设备（如机器人、健康监测设备）能够在线适应分布偏移，提升实际部署的鲁棒性。

## 二、方法论：核心思想、关键技术细节

### 2.1 自集成网络（Self-ensemble Network）
- 将预训练网络（如 ResNet50、MCUNet）按每层激活内存相似度划分为若干子模块（submodules）。
- 每个子模块近似模拟全网络能力，只保留前向传播，反向传播仅更新紧接的退出头（early-exit heads），无需存储全网络激活值，显著降低内存。

### 2.2 早退策略（Early-exits）
- 每个子模块后附加一个线性分类器（含 WS 层）。
- 对输入样本，计算当前子模块输出的熵（公式 2）：\( H(x_i) = -\sum p_k^j \log p_k^j \)。
- 若熵低于预设阈值 \(\gamma_k\)，则认为置信度高，直接从该子模块退出并更新之前所有子模块的头；否则继续向后传播。
- 复杂度低的样本（轻微偏移）在浅层退出，复杂度高的样本（严重偏移）深入全网络，从而适应不同强度偏移，同时减少计算量。

### 2.3 权重标准化（Weight Standardization, WS）
- 替代传统归一化层（BN、GN），直接对权重重心化：\(\tilde{W} = (W - \mu_w)/(\sigma_w + \epsilon)\)，其中 \(\mu_w, \sigma_w\) 为权重的均值和标准差。
- 优点：(1) 不依赖 batch 统计，适用于 batch size=1；(2) 无额外参数，实现简单；(3) 与卷积层可融合，便于 MCU 部署。

### 2.4 TinyTTA Engine
- 基于 TensorFlow Lite Micro 开发的首个支持 MCU 上 TTA 的库。
- 实现浮点算子（ReLU、Conv、FC 等）的反向传播，采用层式更新（layer-wise update）和动态内存分配（heap memory），仅存储需要更新的层的中间激活。

### 2.5 训练与推理流程
- **离线训练**：在源域数据上联合训练所有子模块和早退头，使用两个损失：交叉熵损失 \(L_1\) 和特征对齐损失 \(L_2\)（使子模块特征与预训练模型一致）。
- **在线 TTA**：设备上仅更新早退头（WS + 线性层），其余子模块冻结。推理时根据熵阈值动态选择退出点。

## 三、实验设计

### 3.1 数据集
- **分布偏移数据集**：CIFAR10C、CIFAR100C（15 种 corruptions，5 个等级）。
- **域泛化数据集**：OfficeHome（4 个域，65 类）、PACS（4 个域，7 类）。
- 额外音频数据测试（附录 H）：Speech Commands V2 → Musan Keywords Spotting（含噪声）。

### 3.2 实验平台
- **MPU**：Raspberry Pi Zero 2W（512 MB DRAM）。
- **MCU**：STM32H747（512 KB SRAM，1 MB Flash）。

### 3.3 对比方法
- TENT（调制 BN 层）、CoTTA（全参数更新）、EATA、EcoTTA（自适应 BN + meta network）。
- 非 TTA 基线：TinyEngine（使用 TENT）、偏置微调、TTT。
- 本文方法：TinyTTA（含自集成 + 早退 + WS）。

### 3.4 模型架构
- MCUNet（专为 MCU 优化，2.6 MB）、EfficientNet_b1、MobileNetV2_x05、RegNet-200m。

### 3.5 评估指标
- 准确率、内存峰值（tensor-arena）、每样本延迟（100 批平均）、能耗（Joule）。

## 四、资源与算力

- **训练环境**：Linux 服务器，Intel Xeon Gold 5218 CPU @ 2.30GHz，单张 NVIDIA Quadro RTX 6000 GPU。
- **训练细节**：MCUNet 先在 ImageNet 预训练，再在 CIFAR 上微调 50 轮，额外为早退训练 15 轮。
- **文中未明确说明总训练时长或 GPU 数量**，仅提及训练在标准 GPU 上进行。

## 五、实验数量与充分性

- **主要实验**：四大数据集 × 四种模型 × 多种对比方法，共生成 16 组准确率+内存对比图（图 6）。
- **消融研究**：逐步去除组件（无 WS、无早退+WS、无所有组件），验证各模块贡献（图 7）。
- **额外分析**：
  - 与 TinyEngine（图 9）、偏置微调（图 13）、TTT（图 14）对比。
  - 不同分布偏移等级（L1–L5）表现（图 11）。
  - WS vs GN 对比（图 11）。
  - 音频数据实验（图 12）。
  - MCU 部署资源开销（表 2）。
- **充分性评价**：实验覆盖多种硬件、多种模型、多种数据集和偏移类型，对比方法全面，消融研究完整，结果客观且可复现。但未包含实际机器人或 IoT 场景的端到端测试。

## 六、主要结论与发现

1. **首次在 MCU 上实现高效 TTA**：TinyTTA 是唯一能在 STM32H747（512 KB 内存）上运行的 TTA 方法，且准确率优于所有对比方法。
2. **显著提升准确率**：在 CIFAR100C 上比第二好方法（EcoTTA）高 46.6%，最高提升 57.6%。
3. **内存降低 1.2–6 倍**：相比 TENT（调制），内存减少 2.3 倍；相比 CoTTA 减少 6 倍。
4. **更低的延迟和能耗**：在 Raspberry Pi Zero 2W 上每样本 0.22 秒，能耗 0.44 J，优于 EATA 和 EcoTTA。
5. **WS 优于 GN**：在各级偏移上 WS 均比 GN 准确率高 10–15 个百分点。
6. **早退策略是关键**：无早退的配置准确率下降约 44–54%，内存增加 5 倍。

## 七、优点（亮点）

- **创新性强**：首次将自集成和早退应用于 TTA，并专门针对 MCU 资源约束设计。
- **实用性强**：开发了 TinyTTA Engine 库，可直接部署于主流 MCU（ARM Cortex-M），代码已开源。
- **实验设计全面**：覆盖多种数据集、模型、硬件，并与多种 SOTA 方法公平对比，消融实验充分。
- **理论贡献**：证明了权重标准化（WS）作为 batch-agnostic 归一化在 TTA 中的有效性，克服了 MCU 不支持 BN 的缺陷。
- **显著性能优势**：在极小内存（512 KB）下仍保持高准确率，为边缘 AI 提供了实际可行的适应方案。

## 八、不足与局限

- **实验覆盖有限**：仅测试了 batch size=1 的情况，未探索更大 batch 下的性能；仅测试了图像和音频两种模态，未涵盖视频、IMU 等。
- **训练开销**：需要基于源域数据离线训练自集成模型，无法直接应用于已有预训练模型而不修改。
- **硬件泛化性**：仅在两个具体设备上验证，但文中指出基于 ARM Cortex-M 架构可移植，实际需要更多测试。
- **阈值选择**：熵阈值 \(\gamma_k\) 需根据模型和数据集预调，未提供自适应方法，可能影响部署便利性。
- **动态偏移假设**：假设偏移严重程度不同，但未验证在连续快速变化分布下的鲁棒性（如 Wild-Time 基准）。

（完）
