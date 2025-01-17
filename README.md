# Data Augmentation in Visual RL

**Visual reinforcement learning (RL)** that makes decisions directly from high-dimensional visual inputs has demonstrated significant potential in various domains. However, deploying visual RL techniques to the real world remains challenging due to their **low sample efficiency** and **large generalization gap**. 

To tackle these obstacles, **data augmentation (DA)** has become a widely used technique in visual RL to acquire sample-efficient and generalizable policies by diversifying the training data.

![DA in visual RL](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/c6057fb0b4c6461e2c122c60403aab21479b689e/Image/DA%20in%20visual%20RL.png)

> This repository is based on the paper [**"A Comprehensive Survey of Data Augmentation in Visual Reinforcement Learning"**](https://arxiv.org/abs/2210.04561), authored by Guozheng Ma, [Zhen Wang](https://zhenwang.site/), Zhecheng Yuan, [Xueqian Wang](https://scholar.google.com/citations?user=h9dN_ykAAAAJ&hl=zh-CN), [Bo Yuan](https://scholar.google.com/citations?hl=zh-CN&user=FMiooBoAAAAJ) and [Dacheng Tao](https://scholar.google.com/citations?user=RwlJNLcAAAAJ&hl=zh-CN).
> 
> In this repository, we conduct a systematic collection of existing papers, focusing on [:one: **How to Augment the Data**](#1) and [:two: **How to Leverage the Augmented Data**](#2) in visual RL.
> 
> You can click the button of :bookmark: to jump to the details of corresponding paper!
>
> **The list of related paper will be continuously updated**.
> Welcome to follow this repo! :star:
>
>If this repository is useful to you, please consider citing our paper:
>```
>@article{guozheng2022comprehensive,
>   title={A Comprehensive Survey of Data Augmentation in Visual Reinforcement Learning},
>   author={Guozheng Ma, Zhen Wang, Zhecheng Yuan, Xueqian Wang, Bo Yuan, Dacheng Tao},
>   journal={arXiv preprint arXiv:2210.04561},
>   year={2022}
>}
>```

<div id="1" >

## 1 How to Augment the Data in Visual RL? 
  
The aim of data augmentation (DA) is to increase the amount and diversity of the original training data, so that agents can learn more efficient and robust policies. Thus, a primary focus of previous research is to design effective augmentation approaches.
  
### 1.1 Observation Augmentation, Transition Augmentation and Trajectory Augmentation

Depending on the type of data that the DA technique aims to modify, we divide DA in visual RL into **Observation Augmentation**, **Transition Augmentation** and **Trajectory Augmentation**.


![How to Augment the Data in Visual RL?](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/0da3b5a872e6c93d82afbccd56cd52a0a2db8df3/Image/How%20To%20Aug%20the%20data.png)

| Related Studies |
|--------|
|Rotation, Translation, and Cropping for Zero-Shot Generalization **(CoG 2020)** [*(paper)*](https://ieeexplore.ieee.org/abstract/document/9231907) |
|**[RandFM]** Network Randomization: A Simple Technique for Generalization in Deep Reinforcement Learning **(ICLR 2020)** [*(paper)*](https://arxiv.org/abs/1910.05396) [*(code)*](https://github.com/pokaxpoka/netrand)|
|**[RAD]** Reinforcement Learning with Augmented Data **(NeurIPS 2020)** [*(paper)*](https://proceedings.neurips.cc/paper/2020/hash/e615c82aba461681ade82da2da38004a-Abstract.html) [*(code)*](https://github.com/MishaLaskin/rad) [:bookmark:](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/main/How%20to%20Augment.md)|
|**[MixReg]** Improving Generalization in Reinforcement Learning with Mixture Regularization **(NeurIPS 2020)** [*(paper)*](https://proceedings.neurips.cc/paper/2020/hash/5a751d6a0b6ef05cfe51b86e5d1458e6-Abstract.html) [*(code)*](https://github.com/kaixin96/mixreg) [:bookmark:](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/main/How%20to%20Augment.md)|
|**[PAADA]** Generalization of Reinforcement Learning with Policy-Aware Adversarial Data Augmentation **(ICML 2022 Workshop)** [*(arxiv paper)*](https://arxiv.org/abs/2106.15587) [*(workshop paper)*](https://openreview.net/pdf?id=rzDUUiEFiG) |
|**[MixStyle]** Domain Generalization with MixStyle **(ICLR 2021)** [*(paper)*](https://openreview.net/forum?id=6xHJ37MVxxp) [*(code)*](https://github.com/KaiyangZhou/mixstyle-release)|
|**[PlayVirtual]** Augmenting Cycle-Consistent Virtual Trajectories for Reinforcement Learning **(NeurIPS 2021)** [*(paper)*](https://proceedings.neurips.cc/paper/2021/hash/2a38a4a9316c49e5a833517c45d31070-Abstract.html) [*(code)*](https://github.com/microsoft/Playvirtual) [:bookmark:](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/main/How%20to%20Augment.md)|
|**[CLOP]** Local Feature Swapping for Generalization in Reinforcement Learning **(ICLR 2022)** [*(paper)*](https://openreview.net/forum?id=Sq0-tgDyHe4)|

> Detailed introduction and analysis of the representative studies can be viewed by clicking its :bookmark:.

### 1.2 Automatic Data Augmentation
  
Automatic data augmentation is receiving growing attentions due to the demand of **task-specific augmentation**.
Generally, different tasks benefit from different augmentations, and selecting the most appropriate one requires expert knowledge. Therefore, it is imperative to design a method that can **automatically identify the most effective augmentation method**.

| Related Studies |
|--------|
|**[UCB-DrAC]** Automatic Data Augmentation for Generalization in Reinforcement Learning **(NeurIPS 2021)** [*(paper)*](https://proceedings.neurips.cc/paper/2021/hash/2b38c2df6a49b97f706ec9148ce48d86-Abstract.html) [*(code)*](https://github.com/rraileanu/auto-drac)|
|**[UCB-RAD]** Automatic Data Augmentation by Upper Confidence Bounds for Deep Reinforcement Learning **(ICCAS 2021)** [*(paper)*](https://ieeexplore.ieee.org/abstract/document/9649771)|

### 1.3 Context-aware/Semantic-level Data Augmentation

Another deficiency of current data augmentation methods is that they rely on **pixel-level image transformations**, where each pixel is treated in a **context-agnostic** manner.
However, in visual RL, pixels in the observation are likely to have different levels of relevance to decision making.
This context-agnostic augmentation may mask or destroy the regions in the original observation that are vital for decision-making.
Therefore, it is necessary to incorporate **context awareness** into augmentation.

| Related Studies |
|--------|
|**[EXPAND]** Widening the Pipeline in Human-Guided Reinforcement Learning with Explanation and Context-Aware Data Augmentation **(NeurIPS 2021)** [*(paper)*](https://proceedings.neurips.cc/paper/2021/hash/b6f8dc086b2d60c5856e4ff517060392-Abstract.html) [:bookmark:](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/main/How%20to%20Augment.md)|
|**[TLDA]** Don’t Touch What Matters: Task-Aware Lipschitz Data Augmentation for Visual Reinforcement Learning **(IJCAI 2022)** [*(paper)*](https://arxiv.org/abs/2202.09982) [:bookmark:](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/main/How%20to%20Augment.md)|


<div id="2" >

## 2 How to Leverage the Augmented Data in Visual RL?

The application scenarios where data augmentation plays a vital role can be divided into three cases:

![How to Leverage the Augmented Data](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/4ddbc7b7ccc30330db5436db0963fbb344943e73/Image/How%20to%20Leverage%20the%20Augmented%20Data.png)

- RL agents are trained with task-specific rewards in Case 1 and Case 2, where DA is implemented as an implicit regularization penalty when enlarging the training set.
- However, the effect of implicit regularization is limited and many studies have attempted to design the auxiliary loss to exploit the potential of data augmentation.
- There are also some studies aiming to decouple the representation learning from policy optimization to gain more generalizable policies.
- In Case 3, the environment is explored without any task-specific rewards, and DA can be exploited to learn the task-agnostic representation using unsupervised learning.
 
### 2.1 Implicit Policy Regularization
  
> The definition of implicit and explicit regularization in [:bookmark_tabs:WIKIPEDIA](https://en.wikipedia.org/wiki/Regularization_(mathematics))
>
>> **Explicit regularization** is regularization whenever one explicitly adds a term to the optimization problem. These terms could be priors, penalties, or constraints.
>
>> **Implicit regularization** is all other forms of regularization. This includes, for example, early stopping, using a robust loss function, and discarding outliers.

The initial and naive practice of DA is to expand the training set with augmented (synthesized) samples
This practice introduces prior-based human knowledge into the data, instead of designing explicit penalty terms or modifying the optimization procedure. Hence, it is often classified as a type of **implicit regularization**.
  
![Implicit Policy Regularization](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/f516f033684dc7a9b353f3779a15271c232581e7/Image/Implicit%20Policy%20Regularization.png)
  
| Related Studies |
|--------|
|**[RAD]** Reinforcement Learning with Augmented Data **(NeurIPS 2020)** [*(paper)*](https://proceedings.neurips.cc/paper/2020/hash/e615c82aba461681ade82da2da38004a-Abstract.html) [*(code)*](https://github.com/MishaLaskin/rad) [:bookmark:](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/main/How%20to%20Leverage.md)|
|**[DrQ]** Image Augmentation is All You Need: Regularizing Deep Reinforcement Learning from Pixels **(ICLR 2021)** [*(paper)*](https://openreview.net/forum?id=GY6-6sTvGaf) [*(code)*](https://github.com/denisyarats/drq) [:bookmark:](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/main/How%20to%20Leverage.md)|
|**[DrQ-v2]** Mastering Visual Continuous Control- Improved Data-Augmented Reinforcement Learning **(ICLR 2022)** [*(paper)*](https://openreview.net/forum?id=_SJ-_yyes8) [*(code)*](https://github.com/facebookresearch/drqv2)|
|**[SVEA]** Stabilizing Deep Q-Learning with ConvNets and Vision Transformers under Data Augmentation **(NeurIPS 2021)** [*(paper)*](https://proceedings.neurips.cc/paper/2021/hash/1e0f65eb20acbfb27ee05ddc000b50ec-Abstract.html) [*(code)*](https://github.com/nicklashansen/dmcontrol-generalization-benchmark) [:bookmark:](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/main/How%20to%20Leverage.md)|

-----

### 2.2 Explicit Policy Regularization with Auxiliary Tasks

To further facilitate the representation learning process, we can design auxiliary objectives (with DA) as explicit regularization.
In general, an auxiliary task can be considered as an additional cost-function that the RL agent can predict and observe from the environment in a self-supervised fashion.

For example, the last layer of the network can be split into multiple parts (heads), each working on a specific task.
Multiple heads then propagate errors back to the shared network layers that form the complete representations required by all heads.

![Explicit Policy Regularization with Auxiliary Tasks](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/f516f033684dc7a9b353f3779a15271c232581e7/Image/Explicit%20Policy%20Regularization%20with%20Auxiliary%20Tasks.png)

| Related Studies |
|--------|
|**[CURL]** Contrastive Unsupervised Representations for Reinforcement Learning **(ICML 2020)** [*(paper)*](http://proceedings.mlr.press/v119/laskin20a.html) [*(code)*](https://github.com/MishaLaskin/curl) [:bookmark:](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/main/How%20to%20Leverage.md)|
|**[PI-SAC]** Predictive Information Accelerates Learning in RL **(NeurIPS 2020)** [*(paper)*](https://proceedings.neurips.cc/paper/2020/hash/89b9e0a6f6d1505fe13dea0f18a2dcfa-Abstract.html) [*(code)*](https://github.com/google-research/pisac)|
|**[SPR]** Data-Efficient Reinforcement Learning with Self-Predictive Representations **(ICLR 2021)** [*(paper)*](https://openreview.net/forum?id=uCQfPZwRaUu&fbclid=IwAR3FMvlynXXYEMJaJzPki1x1wC9jjA3aBDC_moWxrI91hLaDvtk7nnnIXT8) [*(code)*](https://github.com/mila-iqia/spr) [:bookmark:](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/main/How%20to%20Leverage.md)|
|**[UCB-DrAC]** Automatic Data Augmentation for Generalization in Reinforcement Learning **(NeurIPS 2021)** [*(paper)*](https://proceedings.neurips.cc/paper/2021/hash/2b38c2df6a49b97f706ec9148ce48d86-Abstract.html) [*(code)*](https://github.com/rraileanu/auto-drac)|
|**[PlayVirtual]** Augmenting Cycle-Consistent Virtual Trajectories for Reinforcement Learning **(NeurIPS 2021)** [*(paper)*](https://proceedings.neurips.cc/paper/2021/hash/2a38a4a9316c49e5a833517c45d31070-Abstract.html) [*(code)*](https://github.com/microsoft/Playvirtual)|
|**[CCFDM]** Sample-efficient Reinforcement Learning Representation Learning with Curiosity Contrastive Forward Dynamics Model **(IROS 2021)** [*(paper)*](https://ieeexplore.ieee.org/abstract/document/9636536)|
|**[SIM]** Generalizing Reinforcement Learning through Fusing Self-Supervised Learning into Intrinsic Motivation **(AAAI 2022)** [*(paper)*](https://www.aaai.org/AAAI22Papers/AAAI-7240.WuK.pdf)|
|**[CRESP]** Learning Task-relevant Representations for Generalization via Characteristic Functions of Reward Sequence Distributions **(KDD 2022)** [*(paper)*](https://arxiv.org/abs/2205.10218) [*(code)*](https://github.com/MIRALab-USTC/RL-CRESP)|
|**[CCLF]** CCLF: A Contrastive-Curiosity-Driven Learning Framework for Sample-Efficient Reinforcement Learning **(IJCAI 2022)** [*(paper)*](https://arxiv.org/abs/2205.00943)|
|**[DRIBO]** DRIBO: Robust Deep Reinforcement Learning via Multi-View Information Bottleneck **(ICML 2022)** [*(paper)*](https://proceedings.mlr.press/v162/fan22b.html) [*(code)*](https://github.com/BU-DEPEND-Lab/DRIBO) [:bookmark:](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/main/How%20to%20Leverage.md)|
|**[CoDy]** Integrating Contrastive Learning with Dynamic Models for Reinforcement Learning from Images **(Neurocomputing 2022)** [*(paper)*](https://www.sciencedirect.com/science/article/abs/pii/S0925231221019500)|
|**[M-CURL]** Masked Contrastive Representation Learning for Reinforcement Learning **(TPAMI 2022)** [*(paper)*](https://ieeexplore.ieee.org/abstract/document/9779589)|
|**[VCD]** Accelerating Representation Learning with View-Consistent Dynamics in Data-Efficient Reinforcement Learning **(arxiv 2022)** [*(paper)*](https://arxiv.org/abs/2201.07016)|
|Does Self-supervised Learning Really Improve Reinforcement Learning from Pixels? **(NeurIPS 2022)** [*(paper)*](https://arxiv.org/abs/2206.05266)|
|**[InDA, ExDA]** Efficient Scheduling of Data Augmentation for Deep Reinforcement Learning **(NeurIPS 2022)** [*(paper)*](https://arxiv.org/abs/2102.08581) [*(code)*](https://github.com/kbc-6723/es-da)|
|**[A2LS]** Reinforcement Learning with Automated Auxiliary Loss Search **(NeurIPS 2022)** [*(paper)*](https://arxiv.org/abs/2210.06041) [*(code)*](https://seqml.github.io/a2ls/)|
|**[MLR]** Mask-based Latent Reconstruction for Reinforcement Learning **(NeurIPS 2022)** [*(paper)*](https://arxiv.org/abs/2201.12096)|[*(code)*](https://github.com/microsoft/Mask-based-Latent-Reconstruction)
 
----
  
### 2.3 Task-Specific Representation Decoupled from Policy Optimization
  

The fragility of RL poses a *dilemma*:
- aggressive augmentations are necessary for achieving good generalization in the visual domain, 
- while injecting heavy data augmentations into the optimization of RL objective may cause a deterioration in both the sample efficiency and the training stability.
  
Recent works argue that this is mainly due to the conflation of two objectives: policy optimization and robust representation learning.
Hence, an intuitive idea is to decouple the training data flow: 
- using non-augmented or weak-augmented data for RL optimization
- while using strong-augmented data for representation learning.

![Task-Specific Representation Decoupled from Policy Optimization](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/1c3a591b5a8448d7dc7786d5dbf65108fd2a466b/Image/Task-Specific%20Representation%20Decoupled%20from%20Policy%20Optimization.png)

| Related Studies |
|--------|
|**[SODA]** Generalization in Reinforcement Learning by Soft Data Augmentation **(ICRA 2021)** [*(paper)*](https://ieeexplore.ieee.org/abstract/document/9561103) [*(code)*](https://github.com/nicklashansen/dmcontrol-generalization-benchmark) [:bookmark:](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/main/How%20to%20Leverage.md)|
|**[SECANT]** Self-Expert Cloning for Zero-Shot Generalization of Visual Policies **(ICML 2021)** [*(paper)*](https://proceedings.mlr.press/v139/fan21c.html) [*(code)*](https://github.com/LinxiFan/SECANT) [:bookmark:](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/main/How%20to%20Leverage.md)|

----
  
### 2.4 Task-Agnostic Representation using Unsupervised Learning
  
The visual representations of standard end-to-end RL methods heavily rely on the task-specific reward, making them ineffective for other tasks.
To overcome this limitation, the environment can be first explored in a **task-agnostic fashion** to learn its visual representations **without any task-specific rewards**, and specific downstream tasks can be subsequently solved efficiently.
  
**DA is exploited as a  key part of unsupervised presentation learning.**

![Task-Agnostic Representation using Unsupervised Learning](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/f516f033684dc7a9b353f3779a15271c232581e7/Image/Task-Agnostic%20Representation%20using%20Unsupervised%20Learning.png)
  
| Related Studies |
|--------|
|**[ATC]** Decoupling Representation Learning from Reinforcement Learning **(ICML 2021)** [*(paper)*](http://proceedings.mlr.press/v139/stooke21a.html) [*(code)*](https://github.com/astooke/rlpyt/tree/master/rlpyt/ul) [:bookmark:](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/main/How%20to%20Leverage.md)|
|**[Proto-RL]** Reinforcement Learning with Prototypical Representations **(ICML 2021)** [*(paper)*](http://proceedings.mlr.press/v139/yarats21a.html) [*(code)*](https://github.com/denisyarats/proto) [:bookmark:](https://github.com/Guozheng-Ma/DA-in-visualRL/blob/main/How%20to%20Leverage.md)|
|**[SGI]** Pretraining Representations for Data-Efficient Reinforcement Learning **(NeurIPS 2021)** [*(paper)*](https://proceedings.neurips.cc/paper/2021/hash/69eba34671b3ef1ef38ee85caae6b2a1-Abstract.html) [*(code)*](https://github.com/mila-iqia/SGI)|
|**[CIC]** CIC: Contrastive Intrinsic Control for Unsupervised Skill Discovery **(arxiv 2022)** [*(paper)*](https://arxiv.org/abs/2202.00161) [*(code)*](https://github.com/rll-research/cic)|

----






