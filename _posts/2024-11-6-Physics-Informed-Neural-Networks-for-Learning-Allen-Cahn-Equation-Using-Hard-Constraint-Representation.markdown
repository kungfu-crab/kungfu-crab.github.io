---
layout: post
title: Physics-Informed Neural Networks for Learning Allen-Cahn Equation Using Hard Constraint Representation
date: 2024-11-6
categories: Research
math: true
---

# Abstract

Lithium-ion batteries have the characteristics of high energy density, good safety, and long cycle life, so they have been widely used in consumer electronics, military, pure electric vehicles, and aerospace in recent years. Learning the electrochemical mechanism equations of lithium-ion batteries is vital for improving battery performance, designing new battery materials, and optimizing battery management systems. The traditional approach models the mechanism of ion migration, diffusion, and charge transfer inside the battery. However, mechanism modeling requires a complete understanding and knowledge of the electrochemical reactions inside the battery, which is very difficult in the research of lithium-ion batteries and even the next generation of new batteries. Therefore, in this paper, the electrochemical mechanistic equations of lithium-ion batteries are learned based on the physics-informed neural network (PINN), and the internal phase separation process of the battery described by the Allen-Cahn equation is used to validate the effectiveness of the proposed method. PINN is a neural network embedded with a physical prior. It restricts the output of the neural network to satisfy the partial differential equations (PDEs) derived from the physical laws by regularizing the loss function. Specifically, this paper uses PINN to perform data-driven learning of 1D and 2D Allen-Cahn equations. It proposes a PINN based on hard constraints to represent the initial conditions (ICs) and boundary conditions (BCs). The Allen-Cahn equation learning results show the proposed approach possesses superior performance over the PINN with soft constraint representation. In addition, we further investigate the effect of the number of sampling points and the performance of different ICs and BCs.

![poster](../assets/poster.jpg)