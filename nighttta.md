---
layout: default
title: Test-Time Adaptation for Nighttime Color-Thermal Semantic Segmentation
---

# Abstract

The ability to scene understanding in adverse visual conditions, e.g., nighttime, has sparked active research for color-thermal semantic segmentation. However, it is essentially hampered by two critical problems: 1) the day-night gap of color images is larger than that of thermal images, and 2) the classwise performance of color images at night is not consistently higher or lower than that of thermal images. We propose the first test-time adaptation (TTA) framework, dubbed Night-TTA, to address the problems for nighttime color-thermal semantic segmentation without access to the source (daytime) data during adaptation. Our method enjoys three key technical parts. Firstly, as one modality (e.g., color) suffers from a larger domain gap than that of the other (e.g., thermal), Imaging Heterogeneity Refinement (IHR) employs an interaction branch on the basis of color and thermal branches to prevent cross-modal discrepancy and performance degradation. Then, Class Aware Refinement (CAR) is introduced to obtain reliable ensemble logits based on pixel-level distribution aggregation of the three branches. In addition, we also design a specific learning scheme for our TTA framework, which enables the ensemble logits and three student logits to collaboratively learn to improve the quality of predictions during the testing phase of our Night TTA. Extensive experiments show that our method achieves state-of-the-art (SoTA) performance with a 13.07% boost in mIoU.
