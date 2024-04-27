---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Computer Generated Holography
======
![CGH](https://github.com/munkyuK/munkyuK.github.io/blob/master/images/CGH.png?raw=true)
Computer-generated holography (CGH) is a technique that generates holograms by computer algorithms. A generated hologram can be displayed by wavefront shaping devices or printed onto a film to get the holographic images. The Gerchberg-Saxton algorithm is a prominent algorithm used for generating holograms. It employs an iterative approach to create the desired phase distribution. I aim to apply a non-iterative point-cloud holography algorithm to a MEMS-based fast Spatial Light Modulator (SLM) for significantly improved speed in scanning points, with the goal of applying it to neuron imaging and optogenetics research.

Reference :
* Nathan Tessema Ersaro, Cem Yalcin, Liz Murray, Leyla Kabuli, Laura Waller, and Rikky Muller, "Fast non-iterative algorithm for 3D point-cloud holography", Optics Express 31, 36468 (2023)

Imaging thorugh Scattering Medium
======
![CLASS](https://github.com/munkyuK/munkyuK.github.io/blob/master/images/CLASS.png?raw=true)
Optical microscopy has suitable conditions for biological imaging. It can resolve sub-cellular structures and is nearly non-invasive because we just illuminate with light and obtain scattered information. However, imaging targets deep inside scattering mediums can be challenging. You cannot directly see inside the skin, or you cannot see far away in foggy conditions. So, why does imaging become difficult in such scenarios?

we can divide the problem into two main aspects. The first is the scattering problem. Imaging can be thought of as measuring the momentum change caused by the target object. Here, the light scattered only once by the sample is called a single scattered wave. Conversely, not only from the object but also from within the medium, we have light that has undergone momentum changes, known as multiple-scattered waves. These waves lose information about the object as they pass through the medium. As the object's depth increases or the scattering becomes more severe, the ballistic wave exponentially decreases, and when the noise level created by multiple scattering exceeds the sample signal, we can no longer distinguish the image.

The other one is the aberration problem. Aberration is angle dependent phase retardation within the single scattering that does not undergo momentum changes. Commonly known as adaptive optics, this is a method to correct system aberrations and restore distorted images. We can do the adaptive optics with hardware such as Shack-Hartmann sensors, or we can computationally correct aberrations. By illuminating the object at various angles we construct a single reflection matrix. We can manage the reflection matrix to accumulate only single scattering coherently and decompose input and output aberrations from obtained datasets, allowing us to restore distorted object images.

Reference :
* S. Kang, S. Jeong et al., "Imaging deep within a scattering medium using collective accumulation of single-scattered waves", Nature Photonics 9, 253-258 (2015)
* S. Kang et al., "High-resolution adaptive optical imaging within thick scattering media using closed-loop accumulation of single scattering", Nature Communications 8, 2157 (2017)

Fourier Holographic Endomicroscopy
======
![bioimaging](https://github.com/munkyuK/munkyuK.github.io/blob/master/images/bioimaging.png?raw=true)
Endoscope is a minimally invasive imaging tool to see inside the human body. There are many types, but here we consider bundle fiber endoscope. Since fiber bundle delivers an image, there is no need to attach a scanner at the distal side. This makes the endoscope thin and robust. However, it is used as fluorescent endoscope because of reflection noise from the probe itself is too strong. Since fluorescence imaging can be limited in medical, here we designed new endoscope system for reflectance imaging.

In conventional reflectance endoscope using bundle fiber, the fiber surface is at the image plane of the target, so the cores act like image pixels. The sample signal and back-reflection noise are captured by the same core, so the image contrast is degraded. Also, you can see the pixelized image because of the spacing between the cores. To resolve this fundamental issue, we placed the distal tip of the fiber at some distance away from the sample. In this case, the back-reflection noise only occurs at an illumination core while the target information is captured by other cores. So we could easily eliminate the back-reflection noise. However, the signals captured at the other cores are in the defocused plane such that they do not form an image by themselves. Furthermore, they experience core-dependent phase retardations depending on the bending and twist of the fiber. We measure holographic image from the fiber and developed novel lensless image reconstruction method that finds and eliminates core-dependent phase retardations in situ.

Reference :
* Wonjun Choi*, Munkyu Kang*, Jin H. Hong, Ori Katz, Byunghak Lee, Guang Hoon Kim, Youngwoon Choi, Wonshik Choi, "Flexible-type ultrathin holographic endoscope for microscopic imaging of unstained biological tissues", Nature Communications., 13, 4469 (2022)
* Munkyu Kang*, Wonjun Choi*, Youngwoon Choi and Wonshik Choi, "Fourier holographic endoscopy for imaging continuously moving objects", Optics Express., 31, 11705 (2023)

Model-based Optimization
======
![Optimization](https://github.com/munkyuK/munkyuK.github.io/blob/master/images/Optimization.png?raw=true)
We can set up a light propagation model that has the same configuration as the experiment. This forward model will be compared with the experimentally recorded electric field and trained to maximize the similarity between them. The optimization algorithm is designed to find three layers in the model, which are object function, input and output aberration. Each starting with random initial values. We employ the Adaptive Moment Estimation (ADAM) optimizer to optimize the complex-valued parameters for minimization of the loss function. With the optimization using Pearson loss, we achieved high-resolution and large FOV of the lensless endoscopic images.

Reference :
* Thi Van Anh Nguyen*, Munkyu Kang*, Dinh Hoang Tran, Tran Thinh Le, Youngwoon Choi, and Wonshik Choi, "Object function retrieval by model-based optimization in Fourier holographic endoscopy", Optics Express., 31, 11705 (2023)

Fourier Ptychography
======
![Ptychography](https://github.com/munkyuK/munkyuK.github.io/blob/master/images/Ptychography.png?raw=true)
In existing imaging systems, there exists a trade-off between the resolution of the captured images and the field of view (FOV). Thus, Fourier Ptychography (FP) has been studied to restore the phase information of objects and enhance spatial bandwidth product using bright-field and dark-field images obtained by illuminating objects from various angles with a low numerical aperture objective lens. FP, utilizing low numerical aperture objective lenses, achieves over two times improvement in optical resolution compared to conventional microscopes using the same objective lens, while maintaining a wide field of view and operating distance. Moreover, it is highly applicable in the field of biomedicine due to its ease of implementation from conventional microscopes. I conducted research on Ptychographic endomicroscopy, which has higher utility, by illuminating a single core through a thin bundle of optical fibers and measuring the reflected object information to restore the phase.

Reference :
* Gil Weinberg, Munkyu Kang, Wonjun Choi, Wonshik Choi, and Ori Katz, "Ptychographic lensless coherent endomicroscopy through a flexible fiber bundle", Optics Express., 31, 11705 (2024)

Three-dimensional holographic imaging of macroscopic objects
======
![SFM](https://github.com/munkyuK/munkyuK.github.io/blob/master/images/SFM.png?raw=true)
Reconstructing real-world objects in three dimensions, such as in autonomous driving or virtual reality, is really interesting and highly practical. Can objects be reconstructed well even in foggy conditions? Is it possible to reconstruct objects behind walls? Many kind of research has been explored such as Non-Line-of-Sight (NLOS) imaging and holography to address these intriguing questions. We have utilized holographic measurement with low-coherence sources to reconstruct objects hidden behind scattering layers. Additionally, in narrow spaces like the oral cavity, we have achieved single-shot multiple depth imaging by multiplexing depth information in the spatial frequency domain, enabling rapid scanning and three-dimensional reconstruction of objects. These advancements open up new possibilities for applications in various fields, from enhancing vision in challenging environments to enabling innovative medical imaging techniques.

Reference :
* Sungsoo Woo, Munkyu Kang, Changhyeong Yoon, Taseok Daniel Yang, Youngwoon Choi and Wonshik Choi, "Three-dimensional imaging of macroscopic objects hidden behind scattering media using time-gated aperture synthesis", Optics Express., 25, 32722 (2017)
* Munkyu Kang*, Sungsoo Woo*, Wonjun Choi*, Pilsung Kang. Tran D. Hoang, Jungsik Koo, Youngwoon Choi and Wonshik Choi, "Single-shot multiple-depth macroscopic imaging by spatial frequency multiplexing", Optics Express., 29, 34360 (2021)


