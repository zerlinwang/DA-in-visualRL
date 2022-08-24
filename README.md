# Data Augmentation in Visual RL

**Visual reinforcement learning (RL)** that makes decisions directly from high-dimensional visual inputs has demonstrated significant potential in various domains. However, deploying visual RL techniques to the real world remains challenging due to their **low sample efficiency** and **large generalization gap**. 

To tackle these obstacles, **data augmentation (DA)** has become a widely used technique in visual RL to acquire sample-efficient and generalizable policies by diversifying the training data.

![DA in visual RL](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/c6057fb0b4c6461e2c122c60403aab21479b689e/Image/DA%20in%20visual%20RL.png)

The Figure above shows **the generic workflow of leveraging DA in visual RL**: diverse augmented data are generated by modifying the original interaction data and then exploited to optimize the **RL objective**. Moreover, DA can improve the representation of visual RL by optimizing **auxiliary representation learning objectives**.

> This repository is based on the paper [**"A Comprehensive Survey of Data Augmentation in Visual Reinforcement Learning"**](), authored by Guozheng Ma, [Zhen Wang](https://zhenwang.site/), Zhecheng Yuan, [Xueqian Wang](https://scholar.google.com/citations?user=h9dN_ykAAAAJ&hl=zh-CN), [Bo Yuan](https://scholar.google.com/citations?hl=zh-CN&user=FMiooBoAAAAJ) and [Dacheng Tao](https://scholar.google.com/citations?user=RwlJNLcAAAAJ&hl=zh-CN).
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
>```
>@article{,
>   title={},
>   author={},
>   journal={},
>   year={2022}
>}
>```


<div id="1" >

## :round_pushpin: How to Augment the Data in Visual RL? [:arrow_forward:](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/780577cfbdbf3aba1e304ca81774cd5af6de857c/How%20to%20Augment.md)
  

The aim of data augmentation (DA) is to increase the amount and diversity of the original training data, so that agents can learn more efficient and robust policies. Thus, a primary focus of previous research is to design effective augmentation approaches.

Depending on the type of data that the DA technique aims to modify, we divide DA in visual RL into **Observation Augmentation**, **Transition Augmentation** and **Trajectory Augmentation**.
  
> Detailed introductions and related studies can be viewed in [:arrow_forward:](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/780577cfbdbf3aba1e304ca81774cd5af6de857c/How%20to%20Augment.md).

![How to Augment the Data in Visual RL?](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/0da3b5a872e6c93d82afbccd56cd52a0a2db8df3/Image/How%20To%20Aug%20the%20data.png)

<div id="2" >

## :triangular_flag_on_post: How to Leverage the Augmented Data in Visual RL?

 
### Implicit Policy Regularization

> **Representative Studies:** [RAD](https://proceedings.neurips.cc/paper/2020/hash/e615c82aba461681ade82da2da38004a-Abstract.html), [DrQ](https://openreview.net/forum?id=GY6-6sTvGaf), [DrQ-v2](), [SVEA]().

![Implicit Policy Regularization](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/f516f033684dc7a9b353f3779a15271c232581e7/Image/Implicit%20Policy%20Regularization.png)
-----

### Explicit Policy Regularization with Auxiliary Tasks

> **Representative Studies:** [CURL](http://proceedings.mlr.press/v119/laskin20a.html), [SPR](https://openreview.net/forum?id=uCQfPZwRaUu&fbclid=IwAR3FMvlynXXYEMJaJzPki1x1wC9jjA3aBDC_moWxrI91hLaDvtk7nnnIXT8), [PlayVirtual](), [DRIBO]().

![Explicit Policy Regularization with Auxiliary Tasks](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/f516f033684dc7a9b353f3779a15271c232581e7/Image/Explicit%20Policy%20Regularization%20with%20Auxiliary%20Tasks.png)
----
  
### Task-Specific Representation Decoupled from Policy Optimization

> **Representative Studies:** [SODA](https://ieeexplore.ieee.org/abstract/document/9561103), [SECANT](https://proceedings.mlr.press/v139/fan21c.html).

![Task-Specific Representation Decoupled from Policy Optimization](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/f516f033684dc7a9b353f3779a15271c232581e7/Image/Task-Specific%20Representation%20Decoupled%20from%20Policy%20Optimization.png)
----
  
### Task-Agnostic Representation using Unsupervised Learning

> **Representative Studies:** [ATC](http://proceedings.mlr.press/v139/stooke21a.html), [Proto-RL](http://proceedings.mlr.press/v139/yarats21a.html).

![Task-Agnostic Representation using Unsupervised Learning](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/f516f033684dc7a9b353f3779a15271c232581e7/Image/Task-Agnostic%20Representation%20using%20Unsupervised%20Learning.png)
----
  
<div id="3" >

## :page_facing_up: Related Paper List 
| 2020 |
|--------|
|**[RandFM]** Network Randomization: A Simple Technique for Generalization in Deep Reinforcement Learning **(ICLR 2020)** [*(paper)*](https://arxiv.org/abs/1910.05396) [*(code)*](https://github.com/pokaxpoka/netrand)|
|**[CURL]** Contrastive Unsupervised Representations for Reinforcement Learning **(ICML 2020)** [*(paper)*](http://proceedings.mlr.press/v119/laskin20a.html) [*(code)*](https://github.com/MishaLaskin/curl)|
|**[RAD]** Reinforcement Learning with Augmented Data **(NeurIPS 2020)** [*(paper)*](https://proceedings.neurips.cc/paper/2020/hash/e615c82aba461681ade82da2da38004a-Abstract.html) [*(code)*](https://github.com/MishaLaskin/rad)|
|**[MixReg]** Improving Generalization in Reinforcement Learning with Mixture Regularization **(NeurIPS 2020)** [*(paper)*](https://proceedings.neurips.cc/paper/2020/hash/5a751d6a0b6ef05cfe51b86e5d1458e6-Abstract.html) [*(code)*](https://github.com/kaixin96/mixreg)|
|Rotation, Translation, and Cropping for Zero-Shot Generalization **(CoG 2020)** [*(paper)*](https://ieeexplore.ieee.org/abstract/document/9231907) |
  
| 2021 |
|--------|
|**[DrQ]** Image Augmentation is All You Need: Regularizing Deep Reinforcement Learning from Pixels **(ICLR 2021)** [*(paper)*](https://openreview.net/forum?id=GY6-6sTvGaf) [*(code)*](https://github.com/denisyarats/drq)|
|**[PAD]** Self-Supervised Policy Adaptation during Deployment **(ICLR 2021)** [*(paper)*](https://openreview.net/forum?id=o_V-MjyyGV_) [*(code)*](https://github.com/nicklashansen/policy-adaptation-during-deployment)|
|**[SPR]** Data-Efficient Reinforcement Learning with Self-Predictive Representations **(ICLR 2021)** [*(paper)*](https://openreview.net/forum?id=uCQfPZwRaUu&fbclid=IwAR3FMvlynXXYEMJaJzPki1x1wC9jjA3aBDC_moWxrI91hLaDvtk7nnnIXT8) [*(code)*](https://github.com/mila-iqia/spr)|
|**[MixStyle]** Domain Generalization with MixStyle **(ICLR 2021)** [*(paper)*](https://openreview.net/forum?id=6xHJ37MVxxp) [*(code)*](https://github.com/KaiyangZhou/mixstyle-release)|
|**[SECANT]** Self-Expert Cloning for Zero-Shot Generalization of Visual Policies **(ICML 2021)** [*(paper)*](https://proceedings.mlr.press/v139/fan21c.html) [*(code)*](https://github.com/LinxiFan/SECANT)|
|**[ATC]** Decoupling Representation Learning from Reinforcement Learning **(ICML 2021)** [*(paper)*](http://proceedings.mlr.press/v139/stooke21a.html) [*(code)*](https://github.com/astooke/rlpyt/tree/master/rlpyt/ul)|
|**[Proto-RL]** Reinforcement Learning with Prototypical Representations **(ICML 2021)** [*(paper)*](http://proceedings.mlr.press/v139/yarats21a.html) [*(code)*](https://github.com/denisyarats/proto)|
|**[SODA]** Generalization in Reinforcement Learning by Soft Data Augmentation **(ICRA 2021)** [*(paper)*](https://ieeexplore.ieee.org/abstract/document/9561103) [*(code)*](https://github.com/nicklashansen/dmcontrol-generalization-benchmark)|
|**[SVEA]** Stabilizing Deep Q-Learning with ConvNets and Vision Transformers under Data Augmentation **(NeurIPS 2021)**|
|**[UCB-DrAC]** Automatic Data Augmentation for Generalization in Reinforcement Learning **(NeurIPS 2021)**|
|**[PlayVirtual]** Augmenting Cycle-Consistent Virtual Trajectories for Reinforcement Learning **(NeurIPS 2021)**|
|**[EXPAND]** Widening the Pipeline in Human-Guided Reinforcement Learning with Explanation and Context-Aware Data Augmentation **(NeurIPS 2021)**|
|**[CCFDM]** Sample-efficient Reinforcement Learning Representation Learning with Curiosity Contrastive Forward Dynamics Model **(IROS 2021)**|
|**[UCB-RAD]** Automatic Data Augmentation by Upper Confidence Bounds for Deep Reinforcement Learning **(ICCAS 2021)**|
|Flexible Data Augmentation in Off-Policy Reinforcement Learning **(ICAISC 2021)**|
|**[PAADA]** Generalization of Reinforcement Learning with Policy-Aware Adversarial Data Augmentation **(arxiv 2021)** |
  
| 2022 |
|--------|
|**[SIM]** Generalizing Reinforcement Learning through Fusing Self-Supervised Learning into Intrinsic Motivation **(AAAI 2022)**|
|**[DrQ-v2]** Mastering Visual Continuous Control- Improved Data-Augmented Reinforcement Learning **(ICLR 2022)**|
|**[CLOP]** Local Feature Swapping for Generalization in Reinforcement Learning **(ICLR 2022)**|
|**[CRESP]** Learning Task-relevant Representations for Generalization via Characteristic Functions of Reward Sequence Distributions **(KDD 2022)**|
|**[TLDA]** Don’t Touch What Matters: Task-Aware Lipschitz Data Augmentation for Visual Reinforcement Learning **(IJCAI 2022)**|
|**[CCLF]** CCLF: A Contrastive-Curiosity-Driven Learning Framework for Sample-Efﬁcient Reinforcement Learning **(IJCAI 2022)**|
|**[DRIBO]** DRIBO: Robust Deep Reinforcement Learning via Multi-View Information Bottleneck **(ICML 2022)**|
|**[CoDy]** Integrating Contrastive Learning with Dynamic Models for Reinforcement Learning from Images **(Neurocomputing 2022)**|
|**[M-CURL]** Masked Contrastive Representation Learning for Reinforcement Learning **(TPAMI 2022)**|
|**[InDA, ExDA]** Efficient Scheduling of Data Augmentation for Deep Reinforcement Learning **(arxiv 2022)** |
|*[MLR]** Mask-based Latent Reconstruction for Reinforcement Learning **(arxiv 2022)** |
|**[VCD]** Accelerating Representation Learning with View-Consistent Dynamics in Data-Efficient Reinforcement Learning **(arxiv 2022)** |
|**[VRL3]** VRL3: A Data-Driven Framework for Visual Deep Reinforcement Learning **(arxiv 2022)** |
|Does Self-supervised Learning Really Improve Reinforcement Learning from Pixels? **(arxiv 2022)** |



