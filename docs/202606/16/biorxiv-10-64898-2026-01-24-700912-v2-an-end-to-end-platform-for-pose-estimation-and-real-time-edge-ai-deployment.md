---
title: An end-to-end platform for pose estimation and real-time edge-AI deployment
title_zh: 一个用于姿态估计和实时边缘AI部署的端到端平台
authors: "Haggerty, D. L., Darden, C. B., Lovinger, D. M."
date: 2026-06-15
pdf: "https://www.biorxiv.org/content/10.64898/2026.01.24.700912v2.full.pdf"
tags: ["query:ur"]
score: 7.0
evidence: 统一的数据集创建与边缘部署平台
tldr: 现有姿态估计工具多面向离线工作流，依赖碎片化软件和高端GPU。本文提出SqueakPose集成软件-硬件生态系统，涵盖数据集创建、模型训练、离线分析和实时边缘部署。系统采用现代目标检测架构，支持CPU/GPU/Apple Silicon，无需补丁采样或多阶段后处理。SqueakView实现实时部署和传感器同步，MouseHouse提供紧凑模块化笼具。该平台无需工作站或中间件，统一离线与实时实验。
source: biorxiv
selection_source: fresh_fetch
motivation: 解决现有姿态估计工具离线、依赖碎片化管线和高性能硬件的问题。
method: 构建集成软件-硬件生态系统，包含SqueakPose Studio、SqueakView和MouseHouse，采用现代目标检测架构实现端到端训练与推理。
result: 支持CPU、GPU及Apple Silicon，无需补丁采样，实现实时边缘部署及同步视频与传感器数据采集。
conclusion: 提供统一平台，降低部署门槛，无缝衔接离线分析与实时实验，无需工作站级硬件或外部中间件。
---

## 摘要
精确的姿态估计支撑着行为的定量分析，然而许多基于深度学习的追踪工具仍针对离线工作流优化，这些工作流依赖于碎片化的软件管道、工作站级GPU或外部中间件来实现实时部署。本文介绍了一个集成的软件-硬件生态系统，用于姿态估计，涵盖数据集创建、模型训练、离线分析以及在嵌入式边缘计算设备上的实时部署。SqueakPose Studio提供了一套用于基于深度学习的整帧姿态估计的软件套件，统一了数据集创建、手动和模型辅助标注、模型训练、验证以及大规模离线推理。该系统利用现代目标检测架构，实现了高效的端到端训练和推理，无需基于补丁的采样或多阶段后处理，并支持在CPU、GPU和Apple Silicon上执行。对于需要连续记录和同步数据采集的实验环境，SqueakView能够在嵌入式边缘计算硬件上实现实时模型部署、视频采集和传感器日志记录，而MouseHouse则提供了一种紧凑的模块化外壳，专为基于家笼的实验设计，集成了嵌入式GPU计算、基于微控制器的定时和外设I/O。共享的数据格式和确定性定时架构确保了离线分析和实时部署之间的一致性。总之，SqueakPose Studio、SqueakView和MouseHouse提供了一个统一的姿态估计平台，支持传统的离线分析和嵌入式实时实验，无需依赖工作站级硬件或外部中间件。

## Abstract
Accurate pose estimation underpins quantitative analysis of behavior, yet many deep learning-based tracking tools remain optimized for offline workflows that rely on fragmented software pipelines, workstation-grade GPUs, or external middleware to enable real-time deployment. Here we present an integrated software-hardware ecosystem for pose estimation that spans dataset creation, model training, offline analysis, and real-time deployment on embedded edge-computing devices. SqueakPose Studio provides a software suite for whole-frame, deep learning-based pose estimation that unifies dataset creation, manual and model-assisted labeling, model training, validation, and large-scale offline inference. The system leverages modern object-detection architectures to enable efficient end-to-end training and inference without patch-based sampling or multi-stage postprocessing, and supports execution on CPUs, GPUs, and Apple Silicon. For experimental settings requiring continuous recording and synchronized data acquisition, SqueakView enables real-time model deployment, video capture, and sensor logging on embedded edge-computing hardware, while MouseHouse provides a compact, modular enclosure designed for home cage-based experiments that integrates embedded GPU compute, microcontroller-based timing, and peripheral I/O. A shared data format and deterministic timing architecture ensure consistency across offline analysis and real-time deployment. Together, SqueakPose Studio, SqueakView, and MouseHouse provide a unified platform for pose estimation that supports both conventional offline analysis and embedded, real-time experimentation, without reliance on workstation-grade hardware or external middleware.