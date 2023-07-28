---
layout: default
title: Factorized Efficient Neural Field Mapping for Real-Time Dense RGB SLAM
description: arxiv
---



<!-- <a href="https://www.youtube.com/watch?v=ty531p2Me7Q">
  <img src="assets/images/cvpr23/egvsr.png" alt="eres" style="width: 500""/>
</a> -->

<!-- [video](https://www.youtube.com/watch?v=ty531p2Me7Qng) -->
[![png](https://i.328888.xyz/2023/03/16/K5vCL.png)](https://www.youtube.com/watch?v=ty531p2Me7Qng)

# Abstract

In this paper, we introduce FMapping, an efficient neural field mapping framework
that facilitates the continuous estimation of a colorized point cloud map in real-time
dense RGB SLAM. To achieve this challenging goal without depth, a hurdle is
how to improve efficiency and reduce the mapping uncertainty of the RGB SLAM
system. To this end, we first build up a theoretical analysis by decomposing the
SLAM system into tracking and mapping parts, and the mapping uncertainty is
explicitly defined within the frame of neural representations. Based on the anal-
ysis, we then propose an effective factorization scheme for scene representation
and introduce a sliding window strategy to reduce the uncertainty for scene re-
construction. Specifically, we leverage the factorized neural field to decompose
uncertainty into a lower-dimensional space, which enhances robustness to noise
and improves training efficiency. We then propose the sliding window sampler
to reduce uncertainty by incorporating coherent geometric cues from observed
frames during map initialization to enhance convergence. Our factorized neural
mapping approach enjoys some advantages, such as low memory consumption,
more efficient computation, and fast convergence during map initialization. Exper-
iments on two benchmark datasets show that our method can update the map of
high-fidelity colorized point clouds around 2 seconds in real time while requiring
no customized CUDA kernels. Additionally, it utilizes ×20 fewer parameters
than the most concise neural implicit mapping of prior methods for SLAM, e.g.,
iMAP and around ×1000 fewer parameters than the state-of-the-art approach,
e.g., NICE-SLAM and DIM-SLAM. 


# Publication

```
@article{fmapHua2023,
  title={FMapping: Factorized Efficient Neural Field Mapping for Real-Time Dense RGB SLAM},
  author={Yunfan Lu, Zipeng Wang, Minjie Liu, Hongjian Wang, Lin Wang},
  year={2023arxiv}
}
```
