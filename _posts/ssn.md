---
layout: post
title: "Revisiting Superpixel Sampling Network: From 2D to 3D"
subtitle: Zhengjie Xu, Shuo Cheng, Quan Vuong
image: ../asset/img/ssn.png
---

Super-pixels provide an efficient low/mid-level represen-tation of image data, which greatly reduces the number of image primitives for subsequent vision tasks. Analogy to super-pixel defined on 2D images, clique on point clouds represents a cluster of points that share the same proper-ties (e.g. colors, semantics, or local geometries). However, existing grouping algorithms are not differentiable, making them hard to be integrated into standard deep neural net-works. Some literatures on clustering algorithms propose to replace the hard assignment with soft association, which makes the grouping step end-to-end trainable.

Samples of Super-pixel segmentation in 2D:
![SS2D](../assets/pdf/ssn-1.png)

Inspired  by  their works,  we propose a novel framework for **D**ifferentiable **P**oint cloud **G**rouping (DPGNet) that allow learning of this useful abstraction through specified downstream tasks. To this end, our contributions are as follows:

- We implement a soft-clustering module for point cloudfeature grouping which enables end-to-end training.
- The proposed soft-clustering module can be easily in-tegrated into standard deep learning framework, which allows learning of task-specific mid-level abstraction.
- We  evaluate our DPGNet on different point cloud analysis tasks on major benchmarks, our experiments demonstrate that the learnt representation can boost the performance of subsequent tasks

![SS3D](../assets/pdf/ssn-2.png)

To learn more about this work, please refer to our [project report](../assets/pdf/ssn.pdf) and [presentation slides](../assets/pdf/ssn-pre.pdf).
