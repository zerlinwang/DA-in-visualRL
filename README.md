# Data Augmentation in Visual RL

**Visual reinforcement learning (RL)** that makes decisions directly from high-dimensional visual inputs has demonstrated significant potential in various domains. However, deploying visual RL techniques to the real world remains challenging due to their **low sample efficiency** and **large generalization gap**. 

To tackle these obstacles, **data augmentation (DA)** has become a widely used technique in visual RL to acquire sample-efficient and generalizable policies by diversifying the training data.

![DA in visual RL](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/c6057fb0b4c6461e2c122c60403aab21479b689e/Image/DA%20in%20visual%20RL.png)

The Figure above shows **the generic workflow of leveraging DA in visual RL**: diverse augmented data are generated by modifying the original interaction data and then exploited to optimize the **RL objective**. Moreover, DA can improve the representation of visual RL by optimizing **auxiliary representation learning objectives**.

> This repository is based on the paper [**"A Comprehensive Survey of Data Augmentation in Visual Reinforcement Learning"**](), authored by Guozheng Ma, [Zhen Wang](https://zhenwang.site/), [Zhecheng Yuan](), [Xueqian Wang](https://scholar.google.com/citations?user=h9dN_ykAAAAJ&hl=zh-CN), [Bo Yuan](https://scholar.google.com/citations?hl=zh-CN&user=FMiooBoAAAAJ) and [Dacheng Tao](https://scholar.google.com/citations?user=RwlJNLcAAAAJ&hl=zh-CN).
> 
> In this repository, we conduct a systematic review of the previous work, focusing on how to obtain and leverage the augmented data in visual RL.
> Also, we present a collection of existing papers on leveraging DA in visual RL scenarios.
> **The list of related paper will be continuously updated**.
> Welcome to follow this repo! :bookmark:
> 
>>**Feel free to skip to the section you're interested in.**
>>
>>[:round_pushpin: **How to Augment the Data in Visual RL?**](#1)
>>
>>[:triangular_flag_on_post: **How to Leverage the Augmented Data in Visual RL?**](#2)
>>
>>[:page_facing_up: **Related Paper List**](#3)
>
>If this repository is useful to you, please consider citing our paper:
>```@article{yuan2022don,
  title={Don't Touch What Matters: Task-Aware Lipschitz Data Augmentationfor Visual Reinforcement Learning},
  author={Yuan, Zhecheng and Ma, Guozheng and Mu, Yao and Xia, Bo and Yuan, Bo and Wang, Xueqian and Luo, Ping and Xu, Huazhe},
  journal={arXiv preprint arXiv:2202.09982},
  year={2022}
  }```


<div id="1" >

## :round_pushpin: How to Augment the Data in Visual RL? [:fast_forward:](How_to_Augment.md)
![How to Augment the Data in Visual RL?](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/eec9c1566047dfc9e35d45d8fb0018c190ba2e9d/Image/How%20To%20Aug%20the%20data.png)

<div id="2" >

## :triangular_flag_on_post: How to Leverage the Augmented Data in Visual RL?
![How to Leverage the Augmented Data in Visual RL?](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/ad52aed2af3bb78d4929f9ede19c05ae259bcae7/Image/How%20to%20Leverage%20the%20Augmented%20Data.png)

<div id="3" >

## :page_facing_up: Related Paper List 

|  Conference  | Paper  |
|  :----:  | ----  |
| ICLR '20 | **[RandFM]** Network Randomization: A Simple Technique for Generalization in Deep Reinforcement Learning [*(paper)*](http://proceedings.mlr.press/v119/laskin20a.html) |
| ICML '20 | **[CURL]** Contrastive Unsupervised Representations for Reinforcement Learning [*(paper)*](https://ieeexplore.ieee.org/abstract/document/9231907)|
| NIPS '20 | **[RAD]** Reinforcement Learning with Augmented Data [*(paper)*](https://ieeexplore.ieee.org/abstract/document/9231907)|
| NIPS '20 | **[MixReg]** Improving Generalization in Reinforcement Learning with Mixture Regularization [*(paper)*](https://ieeexplore.ieee.org/abstract/document/9231907)|
| CoG '20 | Rotation, Translation, and Cropping for Zero-Shot Generalization [*(paper)*](https://ieeexplore.ieee.org/abstract/document/9231907) |
| ICLR '21 | **[DrQ]** Image Augmentation is All You Need: Regularizing Deep Reinforcement Learning from Pixels |
| ICLR '21 | **[PAD]** Self-Supervised Policy Adaptation during Deployment |
| ICLR '21 | **[SPR]** Data-Efficient Reinforcement Learning with Self-Predictive Representations |
| ICLR '21 | **[MixStyle]** Domain Generalization with MixStyle |
| ICML '21 | **[SECANT]** Self-Expert Cloning for Zero-Shot Generalization of Visual Policies |
| ICML '21 | **[ATC]** Decoupling Representation Learning from Reinforcement Learning |
| ICML '21 | **[Proto-RL]** Reinforcement Learning with Prototypical Representations |
| ICRA '21 | **[SODA]** Generalization in Reinforcement Learning by Soft Data Augmentation |
| NIPS '21 | **[SVEA]** Stabilizing Deep Q-Learning with ConvNets and Vision Transformers under Data Augmentation |
| NIPS '21 | **[UCB-DrAC]** Automatic Data Augmentation for Generalization in Reinforcement Learning |
| NIPS '21 | **[PlayVirtual]** Augmenting Cycle-Consistent Virtual Trajectories for Reinforcement Learning |
| NIPS '21 | **[EXPAND]** Widening the Pipeline in Human-Guided Reinforcement Learning with Explanation and Context-Aware Data Augmentation |
| IROS '21 | **[CCFDM]** Sample-efficient Reinforcement Learning Representation Learning with Curiosity Contrastive Forward Dynamics Model |
| ICCAS '21 | **[UCB-RAD]** Automatic Data Augmentation by Upper Confidence Bounds for Deep Reinforcement Learning |
| ICAISC '21 | Flexible Data Augmentation in Off-Policy Reinforcement Learning |
| AAAI '22 | **[SIM]** Generalizing Reinforcement Learning through Fusing Self-Supervised Learning into Intrinsic Motivation |
| ICLR '22 | **[DrQ-v2]** Mastering Visual Continuous Control- Improved Data-Augmented Reinforcement Learning |
| ICLR '22 | **[CLOP]** Local Feature Swapping for Generalization in Reinforcement Learning |
| KDD '22 | **[CRESP]** Learning Task-relevant Representations for Generalization via Characteristic Functions of Reward Sequence Distributions |
| IJCAI '22 | **[TLDA]** Don’t Touch What Matters: Task-Aware Lipschitz Data Augmentation for Visual Reinforcement Learning |
| IJCAI '22 | **[CCLF]** CCLF: A Contrastive-Curiosity-Driven Learning Framework for Sample-Efﬁcient Reinforcement Learning |
| ICML '22 | **[DRIBO]** DRIBO: Robust Deep Reinforcement Learning via Multi-View Information Bottleneck |


|  Journal   | Paper  |
|  :----:  | ----  |
| Neurocomputing&nbsp;‘22 | **[CoDy]** Integrating Contrastive Learning with Dynamic Models for Reinforcement Learning from Images |
| TPAMI ‘22 | **[M-CURL]** Masked Contrastive Representation Learning for Reinforcement Learning |


|  Priprint   | Paper  |
|  :----:  | ----  |
|  arxiv&nbsp;'21 | **[PAADA]** Generalization of Reinforcement Learning with Policy-Aware Adversarial Data Augmentation  |
|  arxiv&nbsp;'22 | **[InDA, ExDA]** Efficient Scheduling of Data Augmentation for Deep Reinforcement Learning  |
|  arxiv '22 | **[MLR]** Mask-based Latent Reconstruction for Reinforcement Learning  |
|  arxiv '22 | **[VCD]** Accelerating Representation Learning with View-Consistent Dynamics in Data-Efficient Reinforcement Learning  |
|  arxiv '22 | **[VRL3]** VRL3: A Data-Driven Framework for Visual Deep Reinforcement Learning  |
|  arxiv '22 | Does Self-supervised Learning Really Improve Reinforcement Learning from Pixels?  |



