---
title: "ANNet: A first-principles neural network for forward and inverse dynamics"
title_zh: ANNet：用于正向和逆向动力学的第一性原理神经网络
authors: "Bahdasariants, S., Parola, L., Kacker, K., Feldman, A. K., Zdobinski, Z., Kang, I., Weber, D. J."
date: 2026-06-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.03.729998v1.full.pdf"
tags: ["query:humanoid-ood"]
score: 6.0
evidence: 使用本体感受信号的物理信息网络进行前向和反向动力学计算
tldr: 生物和机器人系统需要同时求解逆向动力学（由期望运动求力矩）和正向动力学（由力矩求运动），传统上两者被分开建模。本文提出ANNet，一个基于经典力学中Appell加速度能量的物理信息神经网络，通过仅学习一个标量能量函数，逆向动力学通过求导获得，正向动力学则通过优化同一能量函数得到，无需重新训练。在双摆实验上，未训练轨迹的逆解和正解均实时准确，为预测与控制提供了统一表示。
source: biorxiv
selection_source: fresh_fetch
motivation: 逆向与正向动力学传统上被分开建模，忽略了共享的物理结构，导致效率低下且缺乏统一表示。
method: 提出ANNet，学习Appell加速度能量，逆向动力学通过求导能量函数得到，正向动力学通过优化能量函数实现。
result: 在双摆范例中，未训练轨迹的逆解和基于优化的正向模拟均达到实时精度。
conclusion: 该框架为神经科学与机器人中的预测与控制提供了基于第一性原理的统一表示。
---

## 摘要
生物和机器人系统必须解决两个相关的运动计算问题：逆向动力学（确定产生期望运动所需的力或力矩）和正向动力学（将施加的力映射到运动）。尽管这两个计算由相同的运动方程耦合，但在基于模型和数据驱动的方法中，它们通常被估计或实现为不同的逆向和正向映射。这种分离可能掩盖了约束两个问题的共享结构。在这里，我们提出了ANNet，一种物理信息神经网络，通过从经典力学中学习一个标量——阿佩尔加速度能量，将两个计算置于一个共同的习得表示上。该网络将运动学状态和候选加速度映射到这个标量函数，通过将习得的能量函数对加速度求导来恢复关节力矩，从而获得逆向动力学。然后，通过将相同的习得能量景观嵌入到一个优化目标中（其无约束最小值满足吉布斯-阿佩尔方程），无需重新训练即可计算正向动力学。得到的加速度在时间上前向积分。我们在双摆范例上评估了ANNet。在训练期间网络未见过的试验中，基于逆向和优化的正向模拟是实时准确的。我们的结果为使用单一的习得表示来支持预测和控制提供了一条第一性原理路径。

意义：机器人和动物必须解决两个问题才能运动：计算期望运动所需的力或力矩（逆向动力学），以及确定由施加力产生的运动（正向动力学），这两个问题通常被分别建模。我们证明了这两个问题都可以用经典力学中的一个标量函数——阿佩尔加速度能量来表达。训练后的神经网络使该习得函数的导数与参考关节力矩匹配，从而执行逆向动力学。然后，相同的网络通过最小化由习得能量景观构建的目标来计算正向动力学，无需重新训练。这个框架为神经科学和机器人学中的预测和控制提供了统一的表示。

## Abstract
Biological and robotic systems must solve two related computations to move: inverse dynamics, which determines the forces or torques needed to produce a desired movement, and forward dynamics, which maps applied forces to motion. Although these computations are coupled by the same equations of motion, they are usually estimated or implemented as distinct inverse and forward mappings, in both model-based and data-driven formulations. This separation can obscure the shared structure that constrains both problems. Here, we present ANNet, a physics-informed neural network that places both computations on a common learned representation by learning a single scalar quantity from classical mechanics--Appell acceleration energy. The network maps kinematic state and candidate accelerations to this scalar function, and inverse dynamics is obtained by differentiating the learned energy function with respect to acceleration to recover joint torques. Forward dynamics is then calculated without retraining by embedding the same learned energy landscape in an optimization objective whose unconstrained minimum satisfies the Gibbs- Appell equation. The resulting accelerations are integrated forward in time. We evaluate ANNet on a double pendulum paradigm. In trials unseen by the network during training, inverse and optimization-based forward simulations are real-time accurate. Our results provide a first-principles route for using a single learned representation to support both prediction and control.

SignificanceRobots and animals must solve two problems to move: computing the forces or torques needed for a desired motion (inverse dynamics) and determining the motion produced by applied forces (forward dynamics), which are usually modeled separately. We show that both problems can be expressed using a single scalar function from classical mechanics, Appell acceleration energy. A neural network trained so that the derivative of this learned function matches reference joint torques performs inverse dynamics. The same network then computes forward dynamics by minimizing an objective built from the learned energy landscape, without retraining. This framework provides a unified representation for prediction and control in both neuroscience and robotics.