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

The other one is the aberration problem. Aberration is angle dependent phase retardation within the single scattering that does not undergo momentum changes. Commonly known as adaptive optics, this is a method to correct system aberrations and restore distorted images. We can do the adaptive optics with hardware such as Shack-Hartmann sensors, or we can computationally correct aberrations. Input and output aberrations can be decomposed from datasets obtained by illuminating the object at various angles, allowing us to restore distorted object images.

Reference :
* S. Kang, S. Jeong et al., "Imaging deep within a scattering medium using collective accumulation of single-scattered waves", Nature Photonics 9, 253-258 (2015)
* S. Kang et al., "High-resolution adaptive optical imaging within thick scattering media using closed-loop accumulation of single scattering", Nature Communications 8, 2157 (2017)

Fourier Holographic Endomicroscopy
======
![setup_scheme](https://github.com/munkyuK/munkyuK.github.io/blob/master/images/setup_scheme.png?raw=true)


Model-based Optimization
======
![Optimization](https://github.com/munkyuK/munkyuK.github.io/blob/master/images/Optimization.png?raw=true)


Fourier Ptychography
======
![Ptychography](https://github.com/munkyuK/munkyuK.github.io/blob/master/images/Ptychography.png?raw=true)


Computer Generated Holography
======
![CGH](https://github.com/munkyuK/munkyuK.github.io/blob/master/images/CGH.png?raw=true)

