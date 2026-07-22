---
title: Edge-First Ground Reaction Force Estimation with Consumer Smartwatches
title_zh: 基于消费级智能手表的边缘优先地面反作用力估计
authors: "Ghaffarzadeh, P., Chakraborty, D., Aslansefat, K., Dostan, A., Papadopoulos, Y."
date: 2026-07-21
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.18.739307v1.full.pdf"
tags: ["query:humanoid-ood"]
score: 7.0
evidence: 提出紧凑的时间卷积网络并在智能手表/手机边缘端部署，用于时间序列估计，与轻量模型边缘部署用于异常检测相关
tldr: "地面反作用力测量通常限于实验室，无法日常监测。本文提出边缘优先的可穿戴系统，使用两个Apple Watch Series 6分别戴在手腕和腰部，通过GRFNet-MultiScale模型（含扩张残差块和全局上下文分支）在iPhone本地估计垂直GRF。在10名健康受试者的539个站立窗口上，双传感器平均皮尔逊相关0.798，RMSE 257 N，手腕单独配置保留82.5%相关性。成果实现了无云端依赖的本地推断，证明了消费级智能手表可用于日常GRF监测，且早期站立阶段手腕加速度是主要可重复信号。"
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-18-739307-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1771, \"height\": 1624, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-18-739307-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1868, \"height\": 1365, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-18-739307-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 176, \"height\": 342, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-18-739307-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 277, \"height\": 301, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-18-739307-v1/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 276, \"height\": 276, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-18-739307-v1/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 279, \"height\": 192, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-18-739307-v1/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 250, \"height\": 345, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-18-739307-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 959, \"height\": 373, \"label\": \"Table\"}]"
motivation: 突破实验室限制，用消费级智能手表实现日常地面反作用力监测。
method: 双手表采集12通道惯性数据，经GRFNet-MultiScale模型在iPhone本地推断。
result: "双传感器平均皮尔逊相关0.798，RMSE 257 N，手腕单独配置保留82.5%相关性。"
conclusion: 系统在周期性步态中表现良好，手腕加速度是稳定信号源，支持边缘计算。
---

## 摘要
地面反作用力（GRF）测量仍然主要局限于仪器实验室，限制了日常生活中的纵向监测。本文提出了一种边缘优先的可穿戴系统，用于从消费级智能手表估计垂直地面反作用力。两只佩戴在手腕和腰部的Apple Watch Series 6设备以100 Hz的频率将12通道惯性数据流式传输到iPhone，预处理、存储和推理都在本地进行，无需依赖云端。提出的GRFNet-MultiScale模型是一种紧凑的时间卷积网络，具有四个扩张残差块和一个全局上下文分支。在10名健康参与者的539个站立窗口上进行的留一被试评估中，双传感器系统实现了平均皮尔逊相关系数0.798，RMSE为257 N，而仅手腕配置保持了双传感器相关性的82.5%。时间归因在验证折之间保持稳定，并确定早期站立期手腕加速度为主要可重复信号。该系统最适用于周期性运动。

## Abstract
Ground reaction force (GRF) measurement remains largely confined to instrumented laboratories, limiting longitudinal monitoring in daily life. This article presents an edge-first wearable system for estimating vertical GRF from consumer smartwatches. Two Apple Watch Series 6 devices worn at the wrist and waist stream 12-channel inertial data at 100 Hz to an iPhone, where preprocessing, storage, and inference occur locally without cloud dependence. The proposed GRFNet-MultiScale model is a compact temporal convolutional network with four dilated residual blocks and a global context branch. Under leave-one-subject-out evaluation on 539 stance windows from 10 healthy participants, the dual-sensor system achieved a mean Pearson correlation of 0.798 with an RMSE of 257 N, while a wrist-only configuration retained 82.5% of dual-sensor correlation. Temporal attribution remained stable across validation folds and identified early-stance wrist acceleration as the dominant reproducible signal. The system is strongest for cyclic locomotion.