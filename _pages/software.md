---
layout: page
title: Software
permalink: /software
comments: false
---
We have developed and (try to) maintain software for hyperpolarized MRI experiments, RF pulse design, k-space trajectory design, image reconstruction, and educational software.  They are all available on GitHub:

* https://github.com/LarsonLab (Group specific organization)
* https://github.com/UCSF-HMTRC/ (Hyperpolarized MRI organization)
* https://github.com/PulmonaryMRI (Pulmonary MRI organization)

We welcome contributions and collaborators to these repositories.  You can contribute via Pull Requests or Issues through GitHub, or you can reach out to us via email with any interests or comments.

## Hyperpolarized MRI

### Hyperpolarized-MRI-Toolbox

We have compiled and developed a wide range of software tools for hyperpolarized MRI experiments in the [hyperpolarized-mri-toolbox](https://github.com/LarsonLab/hyperpolarized-mri-toolbox).  This includes methods for designing radiofrequency (RF) pulses, imaging gradients, data reconstruction, and data analysis including pharmacokinetic modeling. 

Hyperpolarized-MRI-Toolbox.  Available online at: https://github.com/LarsonLab/hyperpolarized-mri-toolbox doi: 10.5281/zenodo.1198915

### Hyperpolarized Pulse Sequences

We have developed and supported development of pulse sequences for Bruker preclinical MRI and GE Healthcare clinical MRI scanners, as well as in the vendor-agnostic RTHawk Research software.  We also have custom reconstruction pipelines for the RTHawk Research platform that are available.  Since these rely on proprietary source code, they are only available as private repositories.  

Please see https://github.com/UCSF-HMTRC/ for how to request access.


## Pulse Sequence Design

### Spectral-Spatial RF Pulse Design

In the early days of hyperpolarized MRI, a UCSF-Stanford collaboration developed a comprehensive spectral-spatial RF pulse design package, including many optimizations and unpublished methods.  Even though it was started in 2007, I think it's still near state-of-the-art today (2024) :)

https://github.com/LarsonLab/Spectral-Spatial-RF-Pulse-Design

### Long-T2 Suppression Pulses for Ultra-short Echo Time (UTE) MRI

Ultra-short echo time (UTE) and zero echo time (ZTE) magnetic resonance imaging (MRI) allows for visualization of semi-solid tissues with very short T2 relaxation times such as tendons, calcifications, myelin sheaths, and cortical bone, are normally invisible with conventional MRI techniques.
Long-T2 species suppression with RF pulses is one way to improve the contrast of short-T2 species: 

https://github.com/LarsonLab/LongT2-Suppression-Pulses

### Radial-Field-of-Views

Code for designing 3D radial, 3D cones, and PROPELLER k-space trajectories
anisotropic FOV and resolution sampling patterns: 

https://github.com/LarsonLab/Radial-Field-of-Views

## Image Reconstruction

### Motion Management and Lung MRI

Motion management is critical for lung MRI.  We have developed reconstruction methods specifically to manage motion through data-driven motion estimation, estimation motion fields, and iterative reconstructions.  There include
* Soft-gating, Motion-resolved, and Dynamic Image Navigator reconstructions
https://github.com/PulmonaryMRI/pulmonary-MRI-reconstruction
Reference: https://doi.org/10.1002/mrm.26958


* iterative Motion Compensation (iMoCo) reconstruction for MRI. 
https://github.com/PulmonaryMRI/imoco_recon.  Reference: https://doi.org/10.1002/mrm.27998

* Motion-compensated low-rank reconstruction for simultaneous structural and functional UTE lung MRI, https://github.com/PulmonaryMRI/MoCoLoR.  Reference: https://dx.doi.org/10.1002/mrm.29703

### Deep Learning based Image Reconstruction

Deep non-linear inversion (DNLINV) is a scan-specific self-supervised method, meaning no training data is required, that utilizes Bayesian deep learning for undersampled MRI image reconstruction even without calibration data. Pre-print: https://arxiv.org/abs/2203.00361

https://github.com/LarsonLab/dnlinv

## Educational Software

Prof. Larson and the teaching assistants in Principles of MRI taught at UCSF (Biomedical Imaging 201) have developed a simple software package to reinforce and explore the basic principles of MRI.  

MRI-education-resources https://github.com/LarsonLab/MRI-education-resources