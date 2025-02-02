<details>
<summary>DiffPIR: Denoising Diffusion Models for Plug-and-Play Image Restoration (05.2023)</summary>

---

**Publication Date:**

- May 15, 2023

**Conference/Publication:**

- CVPR workshop NTIRE 2023

**Authors:**

- Yuanzhi Zhu, Kai Zhang, Jingyun Liang, Jiezhang Cao, Bihan Wen, Radu Timofte, Luc Van Gool

**Keywords/Tags:**

- Plug-and-play Image Restoration (IR)
- Diffusion models
- Generative denoiser prior
- Neural Function Evaluations (NFEs)
- Super-resolution

**Abstract/Description:**

- The paper delves into the realm of Plug-and-play Image Restoration (IR), a recognized methodology for addressing various inverse problems by leveraging off-the-shelf denoisers. The novelty introduced is "DiffPIR", a method that synergizes the traditional plug-and-play approach with the diffusion sampling framework. The aspiration behind DiffPIR is to harness the generative prowess of diffusion models. Preliminary experiments encompassing tasks such as super-resolution, image deblurring, and inpainting have manifested state-of-the-art results on renowned datasets like FFHQ and ImageNet.

**Highlights/Key Takeaways:**

- Diffusion models, while exemplary for high-quality image synthesis, have been underexplored in the context of serving as generative denoiser priors for plug-and-play IR methods.
- DiffPIR is a pioneering attempt to bridge this gap, promising to amalgamate the generative capabilities of diffusion models.
- Empirical evidence suggests DiffPIR's superiority on datasets like FFHQ and ImageNet, benchmarking its performance against contemporaneous methods.

**Main Concepts:**

- The paper underscores the versatility of Plug-and-play Image Restoration (IR) methods, emphasizing their efficacy across a spectrum of low-level vision tasks.
- A salient feature is the integration of Gaussian denoisers into iterative processes, a strategy that has empirically shown to bolster both performance and convergence.
- The foundational premise of plug-and-play IR pivots on bifurcating the data term and the prior term, a strategy that has been elucidated in the paper.

**Architecture & Methods:**

- DiffPIR is not just a mere integration but a sophisticated fusion of the traditional plug-and-play paradigm into the diffusion sampling framework, aiming to capitalize on the generative attributes of diffusion models.

**Datasets:**

The research leverages two datasets for empirical validation:

- FFHQ
- ImageNet

**Results & Achievements:**

- DiffPIR has set a new benchmark, achieving unparalleled performance on both the FFHQ and ImageNet datasets. This is gauged in terms of both reconstruction fidelity and perceptual quality, all within a constraint of 100 NFEs.

**References:**

- [paper](https://arxiv.org/pdf/2305.08995.pdf)
- [github](https://github.com/yuanzhi-zhu/DiffPIR)

```
@inproceedings{zhu2023denoising, % DiffPIR
      title={Denoising Diffusion Models for Plug-and-Play Image Restoration},
      author={Yuanzhi Zhu and Kai Zhang and Jingyun Liang and Jiezhang Cao and Bihan Wen and Radu Timofte and Luc Van Gool},
      booktitle={IEEE Conference on Computer Vision and Pattern Recognition Workshops (NTIRE)},
      year={2023}
}
```

---
  
</details>





<details>
<summary>Omni-SR: Omni-Dimension Feature Aggregation for Lightweight Image Super-Resolution (04.2023)</summary>

---

**Date of Introduction:**

- April 2023

**Conference/Publication:**

- CVPR 2023

**Authors:**

- Not explicitly mentioned in the provided chunks, but typically available on the paper's title page.

**Abstract/Description:**

- The paper introduces the Efficient Non-Local Contrastive Attention (ENLCA) for Single Image Super-Resolution (SISR). The primary challenge addressed is the limitation of Non-Local Attention (NLA) in SISR, which often gives noisy information significant weights and consumes quadratic computational resources. The proposed ENLCA aims to perform long-range visual modeling and leverage more relevant non-local features efficiently. The method consists of two parts: Efficient Non-Local Attention (ENLA) and Sparse Aggregation. ENLA uses a kernel method to approximate the exponential function, achieving linear computational complexity. Sparse Aggregation focuses on informative features, and contrastive learning is applied to further distinguish between relevant and irrelevant features. The proposed architecture, called Efficient Non-Local Contrastive Network (ENLCN), demonstrates superior performance over state-of-the-art methods in SISR.

**Main Concepts:**

- The paper introduces the Omni Self-Attention (OSA) block based on the dense interaction principle, which can simultaneously model pixel-interaction from both spatial and channel dimensions, mining potential correlations across omni-axis (i.e., spatial and channel).
- The paper also presents the Omni-Scale Aggregation Group (OSAG), a multi-scale hierarchical aggregation block designed to achieve tailored encoding of varying scales of texture patterns.

**Architecture & Methods:**

- Omni Self-Attention (OSA): A novel omni-dimension feature aggregation scheme that exploits both spatial and channel axis information simultaneously, offering higher-order receptive field information.
- Omni-Scale Aggregation Group (OSAG): A multi-scale hierarchical aggregation block that builds three cascaded aggregators: local convolution, meso self-attention, and global self-attention, rendering an omni-scale feature extraction capability.

**Training Details:**

- Not explicitly mentioned in the provided chunks, but typically available in the paper's methodology section.

**Metrics:**

- Not explicitly mentioned in the provided chunks, but typically available in the paper's results section.

**Datasets:**

- Not explicitly mentioned in the provided chunks, but typically available in the paper's methodology section.

**Results & Achievements:**
- The proposed Omni-SR framework exhibits superior restoration performance, covering a larger interaction range while maintaining an attractive model size of 792K.

**Code/Implementation:**

- The source code is available at [Omni-SR GitHub Repository](https://github.com/Francis0625/Omni-SR).

**References:**

- [paper](https://arxiv.org/pdf/2304.10244.pdf)
- [github](https://github.com/Francis0625/Omni-SR)

```
@inproceedings{omni_sr,
  title      = {Omni Aggregation Networks for Lightweight Image Super-Resolution},
  author     = {Wang, Hang and Chen, Xuanhong and Ni, Bingbing and Liu, Yutian and Liu jinfan},
  booktitle  = {Conference on Computer Vision and Pattern Recognition},
  year       = {2023}
}
```

---

</details>





<details>
<summary>DiffIR: An Efficient Diffusion Model for Image Restoration (03.2023)</summary>

---
      
**Date of Introduction:**

- March 2023

**Conference/Publication:**

- ArXiv (preprint)

**Authors:**

- Bin Xia, Yulun Zhang, Shiyin Wang, Yitong Wang, Xinglong Wu, Yapeng Tian, Wenming Yang, and Luc Van Gool 2

**Abstract/Description:**

 - The paper introduces an efficient diffusion model for image restoration (DiffIR). Traditional diffusion models require many iterations and computational resources to generate accurate images or latent feature maps. While these models perform well in image synthesis, applying them directly to image restoration can be inefficient. DiffIR addresses this by using a diffusion model to estimate a compact image restoration prior representation (IPR) to guide the network in restoring images. This approach reduces the model size and iteration count, leading to more accurate estimations compared to traditional diffusion models.

**Main Concepts:**

- The inefficiency of traditional diffusion models when applied directly to image restoration.
- Introduction of DiffIR, which uses a diffusion model to estimate a compact IPR to guide image restoration.
- The potential of DiffIR to reduce model size and iteration count, leading to more accurate estimations.

**Architecture & Methods:**

- Compact IR Prior Extraction Network (CPEN): Extracts a compact IR prior representation (IPR) from ground-truth images.
- Dynamic IRformer (DIRformer): Uses the extracted IPR to restore low-quality images. It consists of dynamic transformer blocks in a U-net shape. These blocks include dynamic multi-head transposed attention (DMTA) and dynamic gated feed-forward network (DGFN), which use the IPR as dynamic modulation parameters to add restoration details into feature maps.

**Training Details:**

- DiffIR is trained in two stages: pretraining and training the diffusion model. In pretraining, the CPEN and DIRformer are trained together using ground-truth and low-quality images. In the second stage, the diffusion model is trained to estimate the IPR directly from low-quality images.

**Metrics:**

- Specific metrics are not mentioned in the provided text, but the paper likely uses standard image restoration metrics.

**Datasets:**

- Specific dataset names are not provided in the summary, but the paper likely uses datasets relevant to image restoration tasks.

**Results & Achievements:**

- DiffIR is presented as a more efficient alternative to traditional diffusion models for image restoration. It achieves high-quality restoration results with reduced computational resources.

**Code/Implementation:**

- The source code is available at [DiffIR GitHub Repository](https://github.com/Zj-BinXia/DiffIR).

**References:**

- [paper](https://arxiv.org/pdf/2303.09472.pdf)
- [github](https://github.com/Zj-BinXia/DiffIR)

```
@article{diffir2023efficient,
    title={DiffIR: An Efficient Diffusion Model for Image Restoration},
    journal={arXiv preprint},
    year={2023}
}
```

---

</details>





<details>
<summary>KDSRGAN: Knowledge Distillation Based Degradation Estimation for Blind Super-Resolution (02.2023)</summary>

---

**Date of Introduction:**

- February 16, 2023
  
**Conference/Publication:**

- ICLR 2023

**Authors:**

- Bin Xia, Yulun Zhang, Yitong Wang, Yapeng Tian, Wenming Yang, Radu Timofte, Luc Van Gool
  
**Abstract/Description:**

- The paper addresses the challenge of blind image super-resolution (Blind-SR), which aims to recover a high-resolution (HR) image from a low-resolution (LR) image with unknown degradations. Traditional methods often rely on explicit degradation estimators for specific degradation processes, making them less adaptable to different degradation types. This work introduces the Knowledge Distillation based Blind-SR network (KDSR) that leverages an implicit degradation estimator to extract degradation representation without needing ground-truth degradation supervision. The proposed method achieves state-of-the-art performance and can adapt to various degradation processes.

**Main Concepts:**

- The significance of degradation models in Blind-SR.
- The limitations of explicit degradation estimators in traditional Blind-SR methods.
- The introduction of an implicit degradation representation (IDR) learning framework for Blind-SR.

**Architecture & Methods:**

- KD-IDE (Knowledge Distillation based Implicit Degradation Estimator): An estimator that predicts accurate implicit degradation representation (IDR) without relying on ground-truth degradation.
- IDR-DCRB (IDR-based Dynamic Convolution Residual Blocks): An efficient SR network designed to utilize the IDR for super-resolution.

**Training Details:**

- The KDSR model involves a two-stage training process. Initially, a teacher network is trained with paired HR and LR images. Subsequently, a student network is trained to extract the same IDR as the teacher network from LR images directly.

**Metrics:**

- While specific metrics are not detailed in the provided summary, the paper likely employs standard super-resolution evaluation metrics.

**Datasets:**

- The exact datasets used are not specified in the summary, but given the context, diverse datasets representing various degradation types are likely used.

**Results & Achievements:**

- KDSR demonstrates superior performance in different degradation settings, from simple to complex, showcasing its adaptability and effectiveness.

**Code/Implementation:**

- The source code is available at [KDSR GitHub Repository](https://github.com/Zj-BinXia/KDSR).

**References:**

- [paper](https://arxiv.org/pdf/2211.16928.pdf)
- [github](https://github.com/Zj-BinXia/KDSR)

```
@InProceedings{xia2022knowledge,
  title={Knowledge Distillation based Degradation Estimation for Blind Super-Resolution},
  author={Xia, Bin and Zhang, Yulun and Wang, Yitong and Tian, Yapeng and Yang, Wenming and Timofte, Radu and Van Gool, Luc},
  journal={ICLR},
  year={2023}
}
```

---
      
</details>





<details>
<summary>SCUNet: Practical Blind Denoising via Swin-Conv-UNet and Data Synthesis (03.2022)</summary>

---

**Date of Introduction:**

- March 28, 2022

**Conference/Publication:**

- ArXiv (preprint)

**Authors:**

- Kai Zhang, Yawei Li, Jingyun Liang, Jiezhang Cao, Yulun Zhang, Hao Tang, Radu Timofte, Luc Van Gool

**Abstract/Description:**

- The paper addresses the challenge of blind image denoising, where most existing methods rely on simple noise assumptions. The authors propose a new approach, DiffPIR, that integrates traditional plug-and-play image restoration into the diffusion sampling framework. The proposed method, Swin-Conv-UNet, combines the strengths of the Swin Transformer and convolutional networks. Additionally, a new noise degradation model is introduced, which considers various types of noise and incorporates strategies like random shuffle and double degradation. The method achieves state-of-the-art performance on various denoising tasks.

**Main Concepts:**

- Challenges with existing denoising methods and their reliance on simple noise assumptions.
- Introduction of Swin-Conv-UNet, which combines local modeling ability of convolutional layers with non-local modeling of Swin Transformer.
- Design of a practical noise degradation model that considers various noise types and incorporates strategies for more realistic training.

**Architecture & Methods:**

- Swin-Conv-UNet (SCUNet): A network that integrates Swin Transformer blocks with convolutional layers. It's designed to capture both local and non-local image features effectively.
- Noise Degradation Model: A model that simulates various types of noise, including Gaussian, Poisson, speckle, JPEG compression, and camera sensor noises. It also uses strategies like random shuffle and double degradation.

**Training Details:**

- The paper emphasizes the importance of a realistic noise model for training. While specific training details are not provided in the summary, the paper likely delves deeper into the training process and parameters.

**Metrics:**

- The paper likely uses standard denoising metrics, though specific metric names are not mentioned in the summary.

**Datasets:**

- The paper mentions the use of various noise types for training, suggesting the use of diverse datasets. Specific dataset names are not provided in the summary.

**Results & Achievements:**

- The proposed Swin-Conv-UNet achieves state-of-the-art performance on denoising tasks.
- The noise degradation model improves the practicability of the denoising model for real images.

**Code/Implementation:**

- The source code is available at [SCUNet GitHub Repository](https://github.com/cszn/SCUNet).

**References:**

- [paper](https://arxiv.org/pdf/2203.13278.pdf)
- [github](https://github.com/cszn/SCUNet)

```
@article{zhang2022practical,
title={Practical Blind Denoising via Swin-Conv-UNet and Data Synthesis},
author={Zhang, Kai and Li, Yawei and Liang, Jingyun and Cao, Jiezhang and Zhang, Yulun and Tang, Hao and Timofte, Radu and Van Gool, Luc},
journal={arXiv preprint},
year={2022}
}
```

---
      
</details>





<details>
<summary>BSRGAN: Designing a Practical Degradation Model for Deep Blind Image Super-Resolution (03.2021)</summary>

---

**Date of Introduction:**

- March 14, 2021 (arXiv:2103.14006v2 [eess.IV] 30 Sep 2021)

**Conference/Publication:**

- ICCV 2021

**Authors:**

- Kai Zhang, Jingyun Liang, Luc Van Gool, Radu Timofte

**Abstract/Description:**

- The paper emphasizes the importance of the degradation model in single image super-resolution (SISR) methods. Existing models may not perform well if the assumed degradation deviates from real images. The authors propose a more complex but practical degradation model that considers randomly shuffled blur, downsampling, and noise degradations. This model aims to cover the diverse degradations of real images. The paper also introduces a deep blind ESRGAN super-resolver trained with this degradation model, demonstrating its effectiveness in real SISR applications.

**Main Concepts:**

- Importance of the degradation model in SISR methods.
- Challenges with existing SISR methods and their assumptions.
- Introduction of a new degradation model that considers diverse degradations of real images.

**Architecture & Methods:**

- Degradation Model: The proposed model considers blur (approximated by two convolutions with isotropic and anisotropic Gaussian kernels), downsampling (chosen from nearest, bilinear, and bicubic interpolations), and noise (Gaussian noise, JPEG compression, and camera sensor noise).
- Random Shuffle Strategy: Instead of the traditional blur/downsampling/noise-addition pipeline, the authors propose a random shuffle strategy for these degradations.
- Deep Blind ESRGAN: A super-resolver trained using the new degradation model.

**Training Details:**

- The paper highlights the use of the new degradation model to synthesize realistic LR images from HR images, providing unlimited paired LR/HR training data without misalignment issues.

**Metrics:**

- Specific metrics are not mentioned in the summary, but the paper likely uses standard SISR metrics.

**Datasets:**

- The degradation model is designed to be applicable to real images with diverse degradations. Specific dataset names are not provided in the summary.

**Results & Achievements:**

- The proposed degradation model improves the practicability of deep super-resolvers, making them more applicable to real SISR tasks.

**Code/Implementation:**

- The source code is available at [BSRGAN GitHub Repository](https://github.com/cszn/BSRGAN).

**References:**

- [paper](https://arxiv.org/pdf/2103.14006.pdf)
- [github](https://github.com/cszn/BSRGAN)

```
@inproceedings{zhang2021designing,
    title={Designing a Practical Degradation Model for Deep Blind Image Super-Resolution},
    author={Zhang, Kai and Liang, Jingyun and Van Gool, Luc and Timofte, Radu},
    booktitle={IEEE International Conference on Computer Vision},
    pages={4791--4800},
    year={2021}
}
```

---
      
</details>





<details>
<summary>SRFBN (2019)</summary>

      
</details>





<details>
<summary>SAN (2019)</summary>

      
</details>





<details>
<summary>Meta-RDN (2019)</summary>

      
</details>





<details>
<summary>RNAN (2019)</summary>

      
</details>





<details>
<summary>ESRGAN (2018)</summary>

      
</details>





<details>
<summary>RCAN (2018)</summary>

      
</details>





<details>
<summary>MSRN (2018)</summary>

      
</details>





<details>
<summary>CARN (2018)</summary>

      
</details>





<details>
<summary>RDN (2018)</summary>

      
</details>





<details>
<summary>DSRN (2018)</summary>

      
</details>





<details>
<summary>DBPN (2018)</summary>

      
</details>





<details>
<summary>SRDenseNet (2017)</summary>

      
</details>





<details>
<summary>MemNet (2017)</summary>

      
</details>





<details>
<summary>EnhanceNet (2017)</summary>

      
</details>





<details>
<summary>EDSR (2017)</summary>

      
</details>





<details>
<summary>SRGAN (2017)</summary>

      
</details>





<details>
<summary>SRResNet (2017)</summary>

      
</details>





<details>
<summary>DRRN (2017)</summary>

      
</details>





<details>
<summary>LapSRN (2017)</summary>

      
</details>





<details>
<summary>ESPCN (2017)</summary>

      
</details>





<details>
<summary>FSRCNN (2016)</summary>

      
</details>





<details>
<summary>DRCN (2016)</summary>

      
</details>





<details>
<summary>SRCNN (2014)</summary>

      
</details>
