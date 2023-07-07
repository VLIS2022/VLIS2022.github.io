
# Learning INR for Event-guided Rolling Shutter Frame Correction, Deblur, and Interpolation
Arxiv

# Abstract

Images captured by rolling shutter (RS) cameras under fast camera motion often contain obvious image distortions and blur, which can be modeled as a row-wise combination of a sequence of global shutter (GS) frames within the exposure time. 
Naturally, recovering high-frame-rate GS sharp frames from an RS blur image needs to simultaneously consider RS correction, deblur, and frame interpolation.
Tacking this task is nontrivial, and to our knowledge, no feasible solutions exist by far.
A naive way is to decompose the whole process into separate tasks and simply cascade existing methods; however, this results in cumulative errors and noticeable artifacts. 
Event cameras enjoy many advantages, e.g., high temporal resolution, making them potential for our problem. To this end, we make the first attempt to recover high-frame-rate sharp GS frames from an RS blur image and paired event data. Our key idea is \textit{to learn an implicit neural representation (INR) to directly map the position and time coordinates to RGB values to address the interlocking degradations in the image restoration process}. 
Specifically, we introduce spatial-temporal implicit encoding (STE) to convert an RS blur image and events into a spatial-temporal representation (STR).
To query a specific sharp frame (GS or RS), we embed the exposure time into STR and decode the embedded features to recover a sharp frame.
Moreover, we propose an RS blur image-guided integral loss to better train the network.
Our method is relatively lightweight as it contains only 0.379 M parameters and demonstrates high efficiency as the STE is called only once for any number of interpolation frames.
Extensive experiments show that our method significantly outperforms prior methods addressing only one or two of the tasks.

# Publication

```
@article{lu2023learning,
  title={Learning INR for Event-guided Rolling Shutter Frame Correction, Deblur, and Interpolation},
  author={Lu, Yunfan and Liang, Guoqiang and Wang, Lin},
  journal={arXiv preprint arXiv:2305.15078},
  year={2023}
}
```
