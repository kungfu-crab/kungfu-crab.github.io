---
layout: post
title: Semi-supervised learning for battery cycle life prediction using a smoothed self-attention mechanism
date: 2026-11-13
categories: 科研成果
---

Yixing Wang, Muhammad Arslan Khan, **Pengyu Chen**, Benben Jiang

## Abstract

Lithium-ion batteries are widely deployed in electric vehicles and other energy storage applications, making accurate cycle life prediction crucial for safety, reliability, and cost reduction. In practical battery aging studies, however, obtaining complete lifetime labels requires long-term cycling tests, resulting in scarce labeled data while abundant early-cycle measurements remain unlabeled. This imbalance restricts the applicability of conventional supervised prediction methods and highlights the need for data-efficient modeling strategies, while common semi-supervised methods often fail to stably extract lifetime-related representations from noisy battery time-series due to inappropriate temporal granularity and weak coupling between labeled and unlabeled samples. To address these challenges, this work proposes a semi-supervised ladder-structured neural network with a smoothed self-attention (SSA) mechanism for battery cycle life prediction. The SSA adapts attention modeling to battery time-series by emphasizing informative temporal segments rather than isolated sampling points, while the ladder architecture promotes consistent representation learning across labeled and unlabeled data through multi-level feature regularization. This design enables stable co-training and effective feature extraction under label-scarce conditions. Experimental results on a public battery aging dataset demonstrate that the proposed method consistently outperforms state-of-the-art supervised and semi-supervised approaches in various scenarios. Using only the first 20 cycles as input, the model maintains an average percentage error below 25% across a wide range of labeled–unlabeled ratios, even when labeled samples are severely limited. Further analyses reveal the critical roles of both the temporal feature extraction and ladder-based reconstruction mechanisms, while also demonstrating that unlabeled data distribution substantially influences semi-supervised prediction performance. These results demonstrate that the proposed attention-guided semi-supervised learning provides an effective and data-efficient framework for battery life prediction under scarce-label conditions, with clear implications for practical battery management applications.

## Keywords

Battery cycle life prediction; Data-driven prediction; Early-cycle data; Semi-supervised learning; Self attention

[ScienceDirect 原文](https://www.sciencedirect.com/science/article/pii/S2352152X26049765) · [DOI: 10.1016/j.est.2026.125312](https://doi.org/10.1016/j.est.2026.125312)
