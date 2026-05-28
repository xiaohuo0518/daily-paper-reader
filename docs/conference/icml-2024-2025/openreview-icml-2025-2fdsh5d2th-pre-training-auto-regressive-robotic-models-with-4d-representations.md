---
title: Pre-training Auto-regressive Robotic Models with 4D Representations
title_zh: 通过4D表示预训练自回归机器人模型
authors: "Dantong Niu, Yuvan Sharma, Haoru Xue, Giscard Biamby, Junyi Zhang, Ziteng Ji, Trevor Darrell, Roei Herzig"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=2FDsh5D2Th"
tags: ["query:ur"]
score: 4.0
evidence: 从视频数据中预训练机器人模型
tldr: 本文提出ARM4R，利用从人类视频中学习的4D表示预训练自回归机器人模型，克服了机器人数据标注成本高和表示建模物理世界不足的问题。在多个模拟任务上，预训练模型显著提升了零样本迁移能力，展示了利用大规模视频数据构建机器人基础模型的潜力。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-2fdsh5d2th/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1767, \"height\": 908, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2fdsh5d2th/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1608, \"height\": 903, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2fdsh5d2th/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1747, \"height\": 584, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2fdsh5d2th/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1715, \"height\": 1151, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2fdsh5d2th/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1762, \"height\": 1914, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2fdsh5d2th/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 859, \"height\": 650, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2fdsh5d2th/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1758, \"height\": 756, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-2fdsh5d2th/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 857, \"height\": 649, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-2fdsh5d2th/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1659, \"height\": 415, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-2fdsh5d2th/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1721, \"height\": 609, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-2fdsh5d2th/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 866, \"height\": 373, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-2fdsh5d2th/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 864, \"height\": 251, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-2fdsh5d2th/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 881, \"height\": 233, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-2fdsh5d2th/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 871, \"height\": 258, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-2fdsh5d2th/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 857, \"height\": 247, \"label\": \"Table\"}]"
motivation: 机器人领域缺乏有效的预训练方法，受限于标注成本和表示能力。
method: 从视频提取3D点轨迹编码为4D表示，自回归预训练机器人策略。
result: 预训练模型在多种操作任务上表现优于从零训练，泛化能力更强。
conclusion: 预训练是提升机器人模型泛化性的有效途径，4D表示弥合了视频与机器人数据的鸿沟。
---

## Abstract
Foundation models pre-trained on massive unlabeled datasets have revolutionized natural language and computer vision, exhibiting remarkable generalization capabilities, thus highlighting the importance of pre-training. Yet, efforts in robotics have struggled to achieve similar success, limited by either the need for costly robotic annotations or the lack of representations that effectively model the physical world. In this paper, we introduce ARM4R, an **A**uto-regressive **R**obotic **M**odel that leverages low-level **4**D **R**epresentations learned from human video data to yield a better pre-trained robotic model. Specifically, we focus on utilizing 3D point tracking representations from videos derived by lifting 2D representations into 3D space via monocular depth estimation across time. These 4D representations maintain a shared geometric structure between the points and robot state representations up to a linear transformation, enabling efficient transfer learning from human video data to low-level robotic control. Our experiments show that ARM4R can transfer efficiently from human video data to robotics and consistently improves performance on tasks across various robot environments and configurations.

---

## 论文详细总结（自动生成）

### 论文核心问题与整体含义（研究动机和背景）

- **核心问题**：机器人领域缺乏有效的预训练方法，主要受限于两方面：① 大规模机器人数据标注成本极高，难以获取；② 现有表示无法充分建模物理世界（如空间几何、物体运动等），导致预训练后迁移效果不佳。
- **整体含义**：探索从海量无标注人类视频中学习低层级的4D表示（3D点轨迹），进而预训练机器人模型，以期像NLP/CV领域一样实现强大的泛化能力，降低对机器人数据的依赖。

### 论文提出的方法论

- **核心思想**：通过3D点跟踪任务学习物体在三维空间中的运动，该任务可以从人类视频自动生成伪标签；3D点坐标与机器人状态之间存在线性变换关系，因此可以高效迁移至机器人控制。
- **关键技术细节**：
  - **4D表示**：利用单目深度估计算法将2D图像提升到3D，然后在时间维度上跟踪3D点的位置，形成4D表示（3D + 时间）。
  - **三阶段训练**：
    1. **Stage 1（人类视频预训练）**：在Epic-Kitchens100数据集（76K视频）上训练自回归模型，预测下一帧的3D点位置，学习通用空间动态。
    2. **Stage 2（机器人视频微调）**：使用少量机器人演示视频（约5-10% of Stage1数据）对同一任务（3D点跟踪）进行微调，适配机器人场景和摄像机配置。
    3. **Stage 3（机器人控制微调）**：将输入/输出从3D点替换为机器人状态（如末端执行器位姿、夹爪开合），微调模型以预测未来状态。
  - **模型架构**：
    - 输入：语言指令（CLIP编码器）、当前图像（ViT编码器）、当前3D点坐标（MLP编码）或机器人状态。
    - 核心：因果Transformer（ViT-Base）进行自回归预测，仅对预测token计算L1损失。
    - 输出：下一时间步的3D点或机器人状态。
- **公式/算法流程（文字说明）**：
  - 预训练阶段：π(l, i_{t-C+1:t}, p_{t-C+1:t}) → p_{t+1}
  - 控制阶段：π(l, i_{t-C+1:t}, s_{t-C+1:t}) → s_{t+1}
  - 损失函数：L = (1/n) * || p̂_{t+1} - p*_{t+1} ||₁

### 实验设计

- **数据集与场景**：
  - **模拟环境**：RLBench（12个任务，如开抽屉、拧灯泡、堆叠方块等），使用Franka Emika Panda机器人。
  - **真实机器人**：
    - Kinova Gen3（7-DoF）：13个任务，涵盖拾取、去堆叠、堆叠、拾取与放置、按压等5类操作。
    - Franka Panda（7-DoF）：3个立方体操作任务（拾取、堆叠、去堆叠），用于跨机器人泛化评估。
- **对比方法**：
  - 模拟：Image-BC (ViT)、C2FARM-BC、ManiGaussian、PerAct、LLARVA。
  - 真实：ATM、LLARVA、π0-FAST、OpenVLA、MVP、RPT、Octo等。
- **评价指标**：成功率（Success Rate），每个任务25个episode，3-5次随机种子取平均。

### 资源与算力

- **训练硬件**：4个NVIDIA A6000 GPU（训练），1个NVIDIA A6000 GPU（评估）。
- **训练时长**：文中未明确给出总时长，但提供了各阶段epoch数：Stage 1为520 epoch，Stage 2和Stage 3为10-50 epoch（视任务收敛情况）。未详细说明数据集大小导致的训练天数。
- **备注**：算力信息基本完整，但缺乏具体时间开销。

### 实验数量与充分性

- **实验组数**：
  - 模拟实验：12个任务，每个任务25个episode × 5个种子 → 约1500次评估。
  - 真实实验：Kinova上13个任务 × 25 episode × 3种子，Franka上3个任务 × 25 episode × 3种子。
  - 消融实验：4组（控制阶段1/2的有无）、跨机器人泛化（2种预训练/微调组合）、鲁棒性测试（扰动时间、光照、背景干扰、桌面干扰等）。
  - 额外实验：预训练方法对比、定性3D点跟踪可视化。
- **充分性与公平性**：
  - 实验较充分，覆盖模拟和真实场景，对比的方法包括2D点跟踪、3D体素、VLA等代表性方法。
  - 但真实任务集中在桌面操作，缺乏移动操作或动态交互任务。鲁棒性测试仅在3个简单任务上进行，未覆盖所有任务。另外，对比方法（如ATM、OpenVLA）使用了作者公开的代码和推荐配置，但未对超参数进行详细调优说明，可能存在一定偏差。

### 论文的主要结论与发现

1. **仅使用人类视频预训练即可获得优于部分使用机器人数据预训练的方法**（如OpenVLA），表明4D表示的有效性。
2. **三阶段训练逐级提升性能**：Stage 1（人类视频）带来的提升大于Stage 2（机器人视频），说明大规模人类数据中蕴含的物理知识对机器人控制至关重要。
3. **ARM4R在模拟和真实场景中均显著超越基线**，平均成功率领先约20-50个百分点（如真实场景平均83.1% vs OpenVLA 37.2%）。
4. **跨机器人泛化能力**：在Franka Panda上，使用Kinova视频微调后性能提升19.6%，证明4D表示具有机器人间可迁移性。
5. **鲁棒性良好**：在动态物体扰动、光照变化、背景干扰下性能下降有限。

### 优点

- **方法创新性**：首次将4D点跟踪预训练用于机器人控制，利用人类视频的几何信息，克服了机器人数据稀缺问题。
- **表示有效性**：证明3D点与机器人状态间存在线性变换关系，使预训练知识可以高效迁移。
- **训练高效**：仅需少量机器人数据（每个任务190个演示）即可达到强性能，且预训练完全使用无标注人类视频。
- **泛化性强**：支持跨任务、跨机器人、动态环境，且能在不同摄像角度下工作。
- **实验设计全面**：模拟+真实多任务验证，消融实验、鲁棒性测试、跨机器人泛化均有覆盖。

### 不足与局限

- **表示耦合问题**：3D点跟踪在相机坐标系进行，物体运动与相机运动混合，缺乏世界坐标系下的不变性，可能影响鲁棒性（如摄像角度变化时）。
- **点选择方式粗糙**：使用固定均匀网格采样，易忽略小物体或背景之间差异，未来可改为关注动态或相关点。
- **单视角依赖**：目前仅使用单目RGB图像，对遮挡和深度估计噪声敏感；多视角融合可进一步提升。
- **任务覆盖有限**：真实任务仅包含桌面操作（拾取、堆叠、按压），未涉及移动操作、精细装配或灵巧手等。
- **对比方法调优不足**：部分对比方法（如ATM, OpenVLA）使用默认参数，未在不同任务上进行细致的超参数搜索，可能削弱对比公平性。
- **未提供计算资源详细开销**：如总GPU小时数、预训练数据量等未明确，不利于复现和资源规划。

（完）
