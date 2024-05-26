# Awesome-Inverse-Rendering

This repo collects papers that use **implicit representation** for inverse rendering. 

Part of this repo is referenced from [Awesome-InverseRendering](https://github.com/tkuri/Awesome-InverseRendering/). Thanks to the author for the outstanding contribution.



## Table of contents

- [What is Inverse Rendering](#what-is-inverse-rendering)
- [NeRF-based Inverse Rendering](#nerf-based-inverse-rendering)
- [NeuS-based Inverse Rendering](#neus-based-inverse-rendering)
- [IDR-based Inverse Rendering](#idr-based-inverse-rendering)
- [DMTet-based Inverse Rendering](#dmtet-based-inverse-rendering)
- [TensoRF-based Inverse Rendering](#tensorf-based-inverse-rendering)
- [Diffusion Prior](#diffusion-prior)
- [Point-based Inverse Rendering](#point-based-inverse-rendering)

## What is Inverse Rendering

- [ ] TODO

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

**Publication**: Arxiv 2021

[📄 Paper](https://arxiv.org/abs/2104.13562) | [💻 Code](https://github.com/princeton-computational-imaging/neural_raytracing) 



### 4. NeRFactor: Neural Factorization of Shape and Reflectance Under an Unknown Illumination

**Authors**: Xiuming Zhang, Pratul P. Srinivasan, Boyang Deng, Paul Debevec, William T. Freeman, Jonathan T. Barron

**Publication**: SIGGRAPH Asia 2021

**Note**: It is undoubtedly an awesome piece of work. "Normal Smoothness" originates from this article. My only regret is that I think the authors were aware that the IR framework based on NeRF struggles to decouple shadows and materials, but they did not mention this in the Limitations section. Their scenarios of **reducing light intensity** (Not the same as vanilla NeRF scenes with obvious shadow and indirect illumination) still impacted many subsequent works that focused on novel view synthesis rather than the accuracy of material decoupling. This is very important for relighting to remove artifacts.

[📄 Paper](https://arxiv.org/pdf/2106.01970.pdf) | [🌐 Project Page](https://xiuming.info/projects/nerfactor/) | [💻 Code](https://github.com/google/nerfactor) 



### 5. Neural-PIL: Neural Pre-Integrated Lighting for Reflectance Decomposition

**Authors**: Mark Boss, Varun Jampani, Raphael Braun, Ce Liu, Jonathan T. Barron, Hendrik P.A. Lensch

**Publication**: NeurIPS 2021

[📄 Paper](https://arxiv.org/abs/2110.14373) | [🌐 Project Page](https://markboss.me/publication/2021-neural-pil/) | [💻 Code](https://github.com/cgtuebingen/Neural-PIL) 



### 6. PS-NeRF: Neural Inverse Rendering for Multi-view Photometric Stereo

**Authors**: Wenqi Yang, Guanying Chen, Chaofeng Chen, Zhenfang Chen, Kwan-Yee K. Wong

**Publication**: ECCV 2022

[📄 Paper](https://arxiv.org/abs/2207.11406) | [🌐 Project Page](https://ywq.github.io/psnerf/) | [💻 Code](https://github.com/ywq/psnerf) 



### 7. NeILF: Neural Incident Light Field for Physically-based Material Estimation

**Authors**: Yao Yao, Jingyang Zhang, Jingbo Liu, Yihang Qu, Tian Fang, David McKinnon, Yanghai Tsin, Long Quan

**Publication**: ECCV 2022

[📄 Paper](https://arxiv.org/abs/2203.07182) | [💻 Code](https://github.com/apple/ml-neilf) 



### 8. L-Tracing: Fast Light Visibility Estimation on Neural Surfaces by Sphere Tracing

**Authors**: Ziyu Chen, Chenjing Ding, Jianfei Guo, Dongliang Wang, Yikang Li, Xuan Xiao, Wei Wu, Li Song

**Publication**: ECCV 2022

**Note**: Visibility estimation without training.

[📄 Paper](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136750214.pdf) | [💻 Code](https://github.com/ziyc/L-Tracing) 



### 9. SAMURAI: Shape And Material from Unconstrained Real-world Arbitrary Image collections

**Authors**: Mark Boss, Andreas Engelhardt, Abhishek Kar, Yuanzhen Li, Deqing Sun, Jonathan T. Barron, Hendrik P. A. Lensch, Varun Jampani

**Publication**: NeurIPS 2022

[📄 Paper](https://arxiv.org/abs/2205.15768) | [🌐 Project Page](https://markboss.me/publication/2022-samurai/) | [💻 Code](https://github.com/google/samurai) 

<br>

## NeuS-based Inverse Rendering

### 1. IRON: Inverse Rendering by Optimizing Neural SDFs and Materials from Photometric Images

**Authors**: Kai Zhang, Fujun Luan, Zhengqi Li, Noah Snavely

**Publication**: **CVPR 2022 (Oral)**

**Note**: Based on NeuS.

[📄 Paper](https://arxiv.org/abs/2204.02232) | [🌐 Project Page](https://kai-46.github.io/IRON-website/) | [💻 Code](https://github.com/Kai-46/IRON) 

### 2. NeRO: Neural Geometry and BRDF Reconstruction of Reflective Objects from Multiview Images

**Authors**: Yuan Liu, Peng Wang, Cheng Lin, Xiaoxiao Long, Jiepeng Wang, Lingjie Liu, Taku Komura, Wenping Wang

**Publication**: SIGGRAPH 2023

**Note**: Apply **split-sum** to constrain the learning of **reflective scenes**.

[📄 Paper](https://arxiv.org/abs/2305.17398) | [🌐 Project Page](https://liuyuan-pal.github.io/NeRO/) | [💻 Code](https://github.com/liuyuan-pal/NeRO) 



### 3. SIRe-IR: Inverse Rendering for BRDF Reconstruction with Shadow and Illumination Removal in High-Illuminance Scenes

**Authors**: Ziyi Yang, Yanzhen Chen, Xinyu Gao, Yazhen Yuan, Yu Wu, Xiaowei Zhou, Xiaogang Jin

**Publication**: It will never be accepted loll

**Note**: This is the first paper that directly faces the issue of shadows and materials being unable to be decoupled under strong lighting conditions. The ACES non-linear mapping is crucial for the removal of shadows and indirect illumination.

[📄 Paper](https://arxiv.org/abs/2310.13030) | [💻 Code](https://github.com/ingra14m/SIRe-IR) 



### 4. Inverse Rendering of Glossy Objects via the Neural Plenoptic Function and Radiance Fields (NeP)

**Authors**: Haoyuan Wang, Wenbo Hu, Lei Zhu, Rynson W.H. Lau

**Publication**: CVPR 2024

[📄 Paper]() | [🌐 Project Page](https://www.whyy.site/paper/nep) | [💻 Code](https://github.com/onpix/NeP) 

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

### 2. TensoSDF: Roughness-aware Tensorial Representation for Robust Geometry and Material Reconstruction

**Authors**: Jia Li, Lu Wang, Lei Zhang, Beibei Wang

**Publication**: SIGGRAPH 2024

[📄 Paper](https://arxiv.org/abs/2402.02771) | [🌐 Project Page](https://wangningbei.github.io/2024/TensoSDF.html) | [💻 Code](https://github.com/Riga2/TensoSDF) 

<br>

## Diffusion Prior

### 1. Diffusion Posterior Illumination for Ambiguity-aware Inverse Rendering (DPI)

**Authors**: Linjie Lyu, Ayush Tewari, Marc Habermann, Shunsuke Saito, Michael Zollhöfer, Thomas Leimkühler, Christian Theobalt

**Publication**: SIGGRAPH Asia 2023

[📄 Paper](https://arxiv.org/abs/2310.00362) | [🌐 Project Page](https://vcai.mpi-inf.mpg.de/projects/2023-DPE/) | [💻 Code](https://github.com/LinjieLyu/DPI)



### 2. IntrinsicAnything: Learning Diffusion Priors for Inverse Rendering Under Unknown Illumination

**Authors**: Xi Chen, Sida Peng, Dongchen Yang, Yuan Liu, Bowen Pan, Chengfei Lv, Xiaowei Zhou

**Publication**: Arxiv 2024

[📄 Paper](https://arxiv.org/abs/2404.11593) | [🌐 Project Page](https://zju3dv.github.io/IntrinsicAnything/) | [💻 Code]()



<br>

## Point-based Inverse Rendering

> From my perspective, I believe that high-quality inverse rendering from a collection of images cannot be achieved with 3D-GS. This is because 3D-GS **lacks robust geometry**, which is fatal for IR. It directly affects the estimation of visibility, limiting the ablitity of decoupling shadows and materials.

### 1. Relightable 3D Gaussian: Real-time Point Cloud Relighting with BRDF Decomposition and Ray Tracing

**Authors**: Jian Gao, Chun Gu, Youtian Lin, Hao Zhu, Xun Cao, Li Zhang, Yao Yao

**Publication**: Arxiv 2023

[📄 Paper](https://arxiv.org/abs/2311.16043) | [🌐 Project Page](https://nju-3dv.github.io/projects/Relightable3DGaussian/) | [💻 Code](https://github.com/NJU-3DV/Relightable3DGaussian) 

### 2. GaussianShader: 3D Gaussian Splatting with Shading Functions for Reflective Surfaces

**Authors**: Yingwenqi Jiang, Jiadong Tu, Yuan Liu, Xifeng Gao, Xiaoxiao Long, Wenping Wang, Yuexin Ma

**Publication**: CVPR 2024

[📄 Paper](https://arxiv.org/abs/2311.17977) | [🌐 Project Page](https://asparagus15.github.io/GaussianShader.github.io/) | [💻 Code](https://github.com/Asparagus15/GaussianShader)

### 3. GS-IR: 3D Gaussian Splatting for Inverse Rendering

**Authors**: Zhihao Liang, Qi Zhang, Ying Feng, Ying Shan, Kui Jia

**Publication**: CVPR 2024

[📄 Paper](https://arxiv.org/abs/2311.16473) | [🌐 Project Page](https://lzhnb.github.io/project-pages/gs-ir.html) | [💻 Code](https://github.com/lzhnb/GS-IR)

### 4. GIR: 3D Gaussian Inverse Rendering for Relightable Scene Factorization

**Authors**:  Yahao Shi, Yanmin Wu, Chenming Wu, Xing Liu, Chen Zhao, Haocheng Feng, Jingtuo Liu, Liangjun Zhang, Jian Zhang, Bin Zhou, Errui Ding, Jingdong Wang

**Publication**: Arxiv 2023

[📄 Paper](https://arxiv.org/abs/2312.05133) | [🌐 Project Page](https://3dgir.github.io/) | [💻 Code (Not yet)]()

### 5. Differentiable Point-based Inverse Rendering

**Authors**: Hoon-Gyu Chung, Seokjun Choi, Seung-Hwan Baek

**Publication**: CVPR 2024

[📄 Paper](https://arxiv.org/abs/2312.02480) | [🌐 Project Page](https://hg-chung.github.io/DPIR/) | [💻 Code](https://github.com/hg-chung/DPIR)

