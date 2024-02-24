# Awesome-Inverse-Rendering

This repo collects papers that use **implicit representation** for inverse rendering. 

Part of this repo is referenced from [Awesome-InverseRendering](https://github.com/tkuri/Awesome-InverseRendering/). Thanks to the author for the outstanding contribution.



## Table of contents

<br>

## What is Inverse Rendering



<br>

## NeRF-based Inverse Rendering

### 1. NeRV: Neural Reflectance and Visibility Fields for Relighting and View Synthesis

**Authors**: Pratul P. Srinivasan, Boyang Deng, Xiuming Zhang, Matthew Tancik, Ben Mildenhall, Jonathan T. Barron

**Publication**: CVPR 2021

**Note**: Assume known environment illumination. Normal estimation from density is from here.

[📄 Paper](https://arxiv.org/abs/2012.03927) | [🌐 Project Page](https://pratulsrinivasan.github.io/nerv/) | [💻 Code (not yet)]() 



### 2. NeRD: Neural Reflectance Decomposition from Image Collections

**Authors**: Mark Boss, Raphael Braun, Varun Jampani, Jonathan T. Barron, Ce Liu, Hendrik P.A. Lensch

**Publication**: ICCV 2021

[📄 Paper](https://arxiv.org/abs/2012.03918) | [🌐 Project Page](https://markboss.me/publication/2021-nerd/) | [💻 Code](https://github.com/cgtuebingen/NeRD-Neural-Reflectance-Decomposition) 



### 3. Neural Ray-Tracing: Learning Surfaces and Reflectance for Relighting and View Synthesis

**Authors**: Julian Knodt, Joe Bartusek, Seung-Hwan Baek, Felix Heide

**Publication**: Arxiv

[📄 Paper](https://arxiv.org/abs/2104.13562) | [💻 Code](https://github.com/princeton-computational-imaging/neural_raytracing) 



### 4. NeRFactor: Neural Factorization of Shape and Reflectance Under an Unknown Illumination

**Authors**: Xiuming Zhang, Pratul P. Srinivasan, Boyang Deng, Paul Debevec, William T. Freeman, Jonathan T. Barron

**Publication**: Siggraph Asia 2021

**Note**: It is undoubtedly an awesome piece of work. "Normal Smoothness" originates from this article. My only regret is that I think the authors were aware that the IR framework based on NeRF struggles to decouple shadows and materials, but they did not mention this in the Limitations section. Their scenarios of **reducing light intensity** (Not the same as vanilla NeRF scenes with obvious shadow and indirect illumination) still impacted many subsequent works that focused on novel view synthesis rather than the accuracy of material decoupling. This is very important for relighting to remove artifacts.

[📄 Paper](https://arxiv.org/pdf/2106.01970.pdf) | [🌐 Project Page](https://xiuming.info/projects/nerfactor/) | [💻 Code](https://github.com/google/nerfactor) 



### 5. Neural-PIL: Neural Pre-Integrated Lighting for Reflectance Decomposition

**Authors**: Mark Boss, Varun Jampani, Raphael Braun, Ce Liu, Jonathan T. Barron, Hendrik P.A. Lensch

**Publication**: NeurIPS 2021

[📄 Paper](https://arxiv.org/abs/2110.14373) | [🌐 Project Page](https://markboss.me/publication/2021-neural-pil/) | [💻 Code](https://github.com/cgtuebingen/Neural-PIL) 



### 6. IRON: Inverse Rendering by Optimizing Neural SDFs and Materials from Photometric Images

**Authors**: Kai Zhang, Fujun Luan, Zhengqi Li, Noah Snavely

**Publication**: **CVPR 2022 (Oral)**

**Note**: Based on NeuS.

[📄 Paper](https://arxiv.org/abs/2204.02232) | [🌐 Project Page](https://kai-46.github.io/IRON-website/) | [💻 Code](https://github.com/Kai-46/IRON) 



### 7. PS-NeRF: Neural Inverse Rendering for Multi-view Photometric Stereo

**Authors**: Wenqi Yang, Guanying Chen, Chaofeng Chen, Zhenfang Chen, Kwan-Yee K. Wong

**Publication**: ECCV 2022

[📄 Paper](https://arxiv.org/abs/2207.11406) | [🌐 Project Page](https://ywq.github.io/psnerf/) | [💻 Code](https://github.com/ywq/psnerf) 



### 8. NeILF: Neural Incident Light Field for Physically-based Material Estimation

**Authors**: Yao Yao, Jingyang Zhang, Jingbo Liu, Yihang Qu, Tian Fang, David McKinnon, Yanghai Tsin, Long Quan

**Publication**: ECCV 2022

[📄 Paper](https://arxiv.org/abs/2203.07182) | [💻 Code](https://github.com/apple/ml-neilf) 



### 9. L-Tracing: Fast Light Visibility Estimation on Neural Surfaces by Sphere Tracing

**Authors**: Ziyu Chen, Chenjing Ding, Jianfei Guo, Dongliang Wang, Yikang Li, Xuan Xiao, Wei Wu, Li Song

**Publication**: ECCV 2022

**Note**: Visibility estimation without training.

[📄 Paper](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136750214.pdf) | [💻 Code](https://github.com/ziyc/L-Tracing) 



### 10. SAMURAI: Shape And Material from Unconstrained Real-world Arbitrary Image collections

**Authors**: Mark Boss, Andreas Engelhardt, Abhishek Kar, Yuanzhen Li, Deqing Sun, Jonathan T. Barron, Hendrik P. A. Lensch, Varun Jampani

**Publication**: NeurIPS 2022

[📄 Paper](https://arxiv.org/abs/2205.15768) | [🌐 Project Page](https://markboss.me/publication/2022-samurai/) | [💻 Code](https://github.com/google/samurai) 



### 11. NeRO: Neural Geometry and BRDF Reconstruction of Reflective Objects from Multiview Images

**Authors**: Yuan Liu, Peng Wang, Cheng Lin, Xiaoxiao Long, Jiepeng Wang, Lingjie Liu, Taku Komura, Wenping Wang

**Publication**: Siggraph 2023

**Note**: Apply **split-sum** to constrain the learning of **reflective scenes**.

[📄 Paper](https://arxiv.org/abs/2305.17398) | [🌐 Project Page](https://liuyuan-pal.github.io/NeRO/) | [💻 Code](https://github.com/liuyuan-pal/NeRO) 

<br>

## IDR-based Inverse Rendering

### 1. PhySG: Inverse Rendering with Spherical Gaussians for Physics-based Material Editing and Relighting

**Authors**: Kai Zhang\*, Fujun Luan\*, Qianqian Wang, Kavita Bala, Noah Snavely

**Publication**: CVPR 2021

**Note**: A successful SG (spherical Gaussian) application in the field of inverse rendering. Unfortunately, the isotropic SG modeling of environmental lighting limits its ability to model anisotropic scenes. Regardless, this is a very awesome work.

[📄 Paper](https://arxiv.org/abs/2104.00674) | [🌐 Project Page](https://kai-46.github.io/PhySG-website/) | [💻 Code](https://github.com/Kai-46/PhySG) 



### 2. Modeling indirect illumination for inverse rendering (InvRender)

**Authors**: Yuanqing Zhang, Jiaming Sun1, Xingyi He, Huan Fu, Rongfei Jia, Xiaowei Zhou

**Publication**: CVPR 2022

**Note**: Nice constrain on indirect illumination.

[📄 Paper](https://arxiv.org/abs/2204.06837) | [🌐 Project Page](https://zju3dv.github.io/invrender/) | [💻 Code](https://github.com/zju3dv/InvRender) 

<br>

## DMTet-based Inverse Rendering

### 1. Extracting Triangular 3D Models, Materials, and Lighting From Images (NVDiffrec)

**Authors**: Jacob Munkberg, Jon Hasselgren, Tianchang Shen, Jun Gao, Wenzheng Chen, Alex Evans, Thomas Müller, Sanja Fidler

**Publication**: **CVPR 2022 (Oral)**

[📄 Paper](https://arxiv.org/abs/2111.12503) | [💻 Code](https://github.com/NVlabs/nvdiffrec) 



### 2. Shape, Light, and Material Decomposition from Images using Monte Carlo Rendering and Denoising (NVDiffrecMC)

**Authors**: Jon Hasselgren, Nikolai Hofmann, Jacob Munkberg

**Publication**: NeurIPS 2022

[📄 Paper](https://arxiv.org/abs/2206.03380) | [🌐 Project Page](https://nvlabs.github.io/nvdiffrecmc/) | [💻 Code](https://github.com/NVlabs/nvdiffrecmc) 

<br>

## TensoRF-based Inverse Rendering

### 1. TensoIR: Tensorial Inverse Rendering

**Authors**: Haian Jin, Isabella Liu, Peijia Xu, Xiaoshuai Zhang, Songfang Han, Sai Bi, Xiaowei Zhou, Zexiang Xu, Hao Su

**Publication**: CVPR 2023

[📄 Paper](https://arxiv.org/abs/2304.12461) | [🌐 Project Page](https://haian-jin.github.io/TensoIR/) | [💻 Code](https://github.com/Haian-Jin/TensoIR) 

<br>

## 3D Gaussian Splatting-based Inverse Rendering

> From my perspective, I believe that high-quality inverse rendering from a collection of images cannot be achieved with 3D-GS. This is because 3D-GS **lacks robust geometry**, which is fatal for IR. It directly affects the estimation of visibility, limiting the ablitity of decoupling shadows and materials.

### 1. Relightable 3D Gaussian: Real-time Point Cloud Relighting with BRDF Decomposition and Ray Tracing

**Authors**: Jian Gao, Chun Gu, Youtian Lin, Hao Zhu, Xun Cao, Li Zhang, Yao Yao

**Publication**: Under review

[📄 Paper](https://arxiv.org/abs/2204.06837) | [🌐 Project Page](https://zju3dv.github.io/invrender/) | [💻 Code](https://github.com/zju3dv/InvRender) 

