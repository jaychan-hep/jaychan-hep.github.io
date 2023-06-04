---
layout: page
title: Unfolding
description: Correct for detector effects with ML
img: assets/img/unfolding_illustration.png
importance: 3
category: Machine Learning for High Energy Physics
---

Unfolding is a key procedure in particle physics. It corrects data for detector effects. Traditionally, we "unfold" data by discretizing the targeted phse space into a finite number of bins in both the truth spectrum and the measured spectrum. This comes with the limitation that the binning needs to be determined beforehand. This is not ideal because the optimal binning usually depends on the downstream inference tasks, while we will only be able to optimize the binning for one specific task, which means that the interpretation will be inflexible and difficult to be reused in the future.

We are now developing modern unfolding methods that utilize Machine Learning techniques. These methods, including density-based methods (e.g. GAN, Normalizing Flows, Variational Auto-Encoder, etc.) and classifier-based methods (e.g. OmniFold), allow for unbinned unfolding and at the same are able to perform unfolding at high dimension! In a recent paper, we also proposed a method "Unbinned Profiled Unfolding", which allows for unbinned unfolding and simultaneously constraining nuisance parameters.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/UPU.png" title="example image" class="img-fluid rounded z-depth-1" bkg-white=true zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/UPU_Higgs_w0_theta_pth.pdf" title="example image" class="img-fluid rounded z-depth-1" bkg-white=true zoomable=true %}
    </div>
</div>
<div class="caption">
    (Left) The procedure of the Unbinned Profiled Unfolding. (Right) The result of the Unbinned Profiled Unfolding with an example of Higgs boson differential cross-section measurements (targetting the spectrum of the Higgs boson transverse momentum).
</div>