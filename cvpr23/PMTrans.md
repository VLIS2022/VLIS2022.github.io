---
layout: default
title: Patch-Mix Transformer for Unsupervised Domain Adaptation:A Game Perspective
description: CVPR 2023 (Highlight)
---

<img src="assets/images/cvpr23/egvsr.png" alt="eres" style="width: 500""/>


# Abstract

Endeavors have been recently made to leverage the vision transformer (ViT) for the challenging unsupervised domain adaptation (UDA) task. They typically adopt the cross-attention in ViT for direct domain alignment. However, as the performance of cross-attention highly relies on the quality of pseudo labels for targeted samples, it becomes less effective when the domain gap becomes large. We solve this problem from a game theory’s perspective with the proposed model dubbed as PMTrans, which bridges source and target domains with an intermediate domain. Specifically, we propose a novel ViT-based module called PatchMix that effectively builds up the intermediate domain, i.e., probability distribution, by learning to sample patches from both domains based on the game-theoretical models. This way, it learns to mix the patches from the source and target domains to maximize the cross entropy (CE), while exploiting two semi-supervised mixup losses in the feature and label spaces to minimize it. As such, we interpret the process of UDA as a min-max CE game with three players, including the feature extractor, classifier, and PatchMix, to find the Nash Equilibria. Moreover, we leverage attention maps from ViT to re-weight the label of each patch by its importance, making it possible to obtain more domain-discriminative feature representations. We conduct extensive experiments on four benchmark datasets, and the results show that PMTrans significantly surpasses the ViT-based and CNN-based SoTA methods by +3.6% on Office-Home, +1.4% on Office-31, and +7.2% on DomainNet, respectively.

# Research Problem

How to smoothly bridge the source and target domains by constructing an intermediate domain with an effective ViT-based solution? 

# Method

we propose a novel and effective method, called PMTrans (PatchMix Transformer) to construct the intermediate representations. Overall, PMTrans interprets the process of domain alignment as a min- max cross entropy (CE) game with three players, i.e., the feature extractor, a classifier, and a PatchMix module, to find the Nash Equilibria. Importantly, the PatchMix module is proposed to effectively build up the intermediate domain, i.e., probability distribution, by learning to sample patches from both domains with weights generated from a learnable Beta distribution based on the game-theoretical models.
<div align=center>
<img src="assets/images/cvpr23/pm_1.jpg" width="50%">
</div>

## Patch-Mix

The definition of PatchMix is

<div align=center>
<img src="assets/images/cvpr23/pm_6.png" width="50%">
</div>

The comparison between PatchMix and Mixup variants is shown as

<div align=center>
<img src="assets/images/cvpr23/pm_7.png">
</div>

## A Min-Max CE Game
Each player's cost function in this game is represented as

<div align=center>
<img src="assets/images/cvpr23/pm_5.png" width="50%">
</div>

## Proposed framework
<div align=center>
<img src="assets/images/cvpr23/PM_2.png">
</div>

## Semi-supervised mixup loss
The illustration of two proposed semi-supervised mixup loss is 
<div align=center>
<img src="assets/images/cvpr23/pm-3.png" width="50%">
</div>

# Result
The results on the most challenging dataset DomainNet is shown as
<div align=center>
<img src="assets/images/cvpr23/PM-4.png">
</div>


# Publication

```
@article{zhu23cvpr,
  title={Patch-Mix Transformer for Unsupervised Domain Adaptation: A Game Perspective},
  author={Jinjing Zhu, Haotian Bai, Lin Wang},
  journal={IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},
  year={2023}
}
```
Code is avaliable at [PMTrans](https://github.com/JinjingZhu/PMTrans).
