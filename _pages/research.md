---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

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
![setup_scheme](https://github.com/munkyuK/munkyuK.github.io/blob/master/images/setup_scheme.png?raw=true)
Endoscope is a minimally invasive imaging tool to see inside the human body. There are many types, but here we consider bundle fiber endoscope. Since fiber bundle delivers an image, there is no need to attach a scanner at the distal side. This makes the endoscope thin and robust. However, it is used as fluorescent endoscope because of reflection noise from the probe itself is too strong. Since fluorescence imaging can be limited in medical, here we designed new endoscope system for reflectance imaging.

In conventional reflectance endoscope using bundle fiber, the fiber surface is at the image plane of the target, so the cores act like image pixels. The sample signal and back-reflection noise are captured by the same core, so the image contrast is degraded. Also, you can see the pixelized image because of the spacing between the cores. To resolve this fundamental issue, we placed the distal tip of the fiber at some distance away from the sample. In this case, the back-reflection noise only occurs at an illumination core while the target information is captured by other cores. So we could easily eliminate the back-reflection noise. However, the signals captured at the other cores are in the defocused plane such that they do not form an image by themselves. Furthermore, they experience core-dependent phase retardations depending on the bending and twist of the fiber. We measure holographic image placed some distance away from the fiber and developed novel lensless image reconstruction method that finds and eliminates core-dependent phase retardations in situ.

Reference :
* Wonjun Choi*, Munkyu Kang*, Jin H. Hong, Ori Katz, Byunghak Lee, Guang Hoon Kim, Youngwoon Choi, Wonshik Choi, "Flexible-type ultrathin holographic endoscope for microscopic imaging of unstained biological tissues", Nature Communications., 13, 4469 (2022)
* Munkyu Kang*, Wonjun Choi*, Youngwoon Choi and Wonshik Choi, "Fourier holographic endoscopy for imaging continuously moving objects", Optics Express., 31, 11705 (2023)


Model-based Optimization
======
![Optimization](https://github.com/munkyuK/munkyuK.github.io/blob/master/images/Optimization.png?raw=true)

Reference :
* Thi Van Anh Nguyen*, Munkyu Kang*, Dinh Hoang Tran, Tran Thinh Le, Youngwoon Choi, and Wonshik Choi, "Object function retrieval by model-based optimization in Fourier holographic endoscopy", Optics Express., 31, 11705 (2023)
We can First, we set up three layers, each starting with random initial values. We assumed the illuminating cores to be Gaussian beams and applied the first layer. Next, we performed free space propagation to apply the second layer and again propagated through free space to apply the final layer. In this case, instead of Fresnel propagation, we used angular spectrum propagation to find the exact solution. Then, We trained to minimize the difference between model output and the experimental data.


Fourier Ptychography
======
![Ptychography](https://github.com/munkyuK/munkyuK.github.io/blob/master/images/Ptychography.png?raw=true)

Reference :
* Gil Weinberg, Munkyu Kang, Wonjun Choi, Wonshik Choi, and Ori Katz, "Ptychographic lensless coherent endomicroscopy through a flexible fiber bundle", Optics Express., 31, 11705 (2024)


Computer Generated Holography
======
![CGH](https://github.com/munkyuK/munkyuK.github.io/blob/master/images/CGH.png?raw=true)


Reference :
* Nathan Tessema Ersaro, Cem Yalcin, Liz Murray, Leyla Kabuli, Laura Waller, and Rikky Muller, "Fast non-iterative algorithm for 3D point-cloud holography", Optics Express 31, 36468 (2023)

Three-dimensional holographic imaging of macroscopic objects
======
![SFM](https://github.com/munkyuK/munkyuK.github.io/blob/master/images/SFM.png?raw=true)

Reference :
* Sungsoo Woo, Munkyu Kang, Changhyeong Yoon, Taseok Daniel Yang, Youngwoon Choi and Wonshik Choi, "Three-dimensional imaging of macroscopic objects hidden behind scattering media using time-gated aperture synthesis", Optics Express., 25, 32722 (2017)
* Munkyu Kang*, Sungsoo Woo*, Wonjun Choi*, Pilsung Kang. Tran D. Hoang, Jungsik Koo, Youngwoon Choi and Wonshik Choi, "Single-shot multiple-depth macroscopic imaging by spatial frequency multiplexing", Optics Express., 29, 34360 (2021)


