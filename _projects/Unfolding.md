---
layout: page
title: Unfolding
description: Machine learning methods for correcting detector effects.
img: assets/img/unfolding_illustration.png
importance: 3
category: Machine Learning for High Energy Physics
---

Unfolding estimates particle-level distributions from measurements distorted by a detector. I develop machine learning methods to correct those distortions and account for uncertainties in the detector response.

[**Unbinned Profiled Unfolding**](https://doi.org/10.1103/PhysRevD.108.016002) fits detector nuisance parameters while unfolding a particle-level spectrum. In a simulated Higgs-to-diphoton benchmark, the method recovered the Higgs transverse momentum spectrum and fitted a photon resolution scale of 1.19 ± 0.007 for an injected value of 1.20.

[**Neural Posterior Unfolding**](https://doi.org/10.1088/1748-0221/21/03/P03004) uses normalizing flows to estimate a full posterior distribution. We evaluated the method on synthetic examples and simulated collider jet-substructure data.

{% include figure.html path="assets/img/UPU.png" alt="Diagram of the Unbinned Profiled Unfolding method" class="img-fluid rounded" bkg-white=true caption="Unbinned Profiled Unfolding jointly estimates the spectrum and detector nuisance parameters." %}

[Higgs transverse momentum benchmark (PDF)]({{ '/assets/img/UPU_Higgs_w0_theta_pth.pdf' | relative_url }})
