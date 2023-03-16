---
layout: default
title: Learning Spatial-Temporal Implicit Neural Representations for Event-Guided Video Super-Resolution
description: CVPR 2023
---



<!-- <a href="https://www.youtube.com/watch?v=ty531p2Me7Q">
  <img src="assets/images/cvpr23/egvsr.png" alt="eres" style="width: 500""/>
</a> -->

<!-- [video](https://www.youtube.com/watch?v=ty531p2Me7Qng) -->
[![png](https://i.328888.xyz/2023/03/16/K5vCL.png)](https://www.youtube.com/watch?v=ty531p2Me7Qng)

# Abstract

Event cameras sense the intensity changes asynchronously and produce event streams with high dynamic range and low latency. This has inspired research endeavors utilizing events to guide the challenging video super-resolution (VSR) task. In this paper, we make the first attempt to address a novel problem of achieving VSR at random scales by taking advantages of the high temporal resolution property of events. This is hampered by the difficulties of representing the spatial-temporal information of events when guiding VSR. To this end, we propose a novel framework that incorporates the spatial-temporal interpolation of events to VSR in a unified framework. Our key idea is to learn implicit neural representations from queried spatial-temporal coordinates and features from both RGB frames and events. Our method contains three parts. Specifically, the Spatial-Temporal Fusion (STF) module first learns the 3D features from events and RGB frames. Then, the Temporal Filter (TF) module unlocks more explicit motion information from the events near the queried timestamp and generates the 2D features. Lastly, the Spatial Temporal Implicit Representation (STIR) module recovers the SR frame in arbitrary resolutions from the outputs of these two modules. In addition, we collect a real-world dataset with spatially aligned events and RGB frames. Extensive experiments show that our method significantly surpass the prior-arts and achieves VSR with random scales, e.g., 6.5.



# Publication

```
@article{lu21cvpr,
  title={Learning Spatial-Temporal Implicit Neural Representations for Event-Guided Video Super-Resolution},
  author={Yunfan Lu, Zipeng Wang, Minjie Liu, Hongjian Wang, Lin Wang},
  journal={IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},
  year={2022}
}
```