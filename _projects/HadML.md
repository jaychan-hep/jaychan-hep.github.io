---
layout: page
title: HadML
description: Simulating hadronization with ML-based generative models
img: assets/img/ENP_WEB.jpg
importance: 2
category: Machine Learning for High Energy Physics
---

Hadronization is a critical step in the simulation of high-energy particle and nuclear physics experiments. As there is no first principles understanding of this process, physically-inspired hadronization models have a large number of parameters that are fit to data. Deep generative models are a natural replacement for classical techniques, since they are more flexible and may be able to improve the overall precision. We are developing deeo generative models, or GAN, to simulate particle hadronization. The ultimate goal is to integrate machine learning-based hadronization models into parton shower Monte Carlo programs.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/MLHadv2.pdf" title="example image" class="img-fluid rounded z-depth-1" bkg-white=true zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/loss_vs_epochs.pdf" title="example image" class="img-fluid rounded z-depth-1" bkg-white=true zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/theta_truthframe.pdf" title="example image" class="img-fluid rounded z-depth-1" bkg-white=true zoomable=true %}
    </div>
</div>
<div class="caption">
    (Left) An overview of the current GAN hadronization model. (Middle) The training history of the best GAN model. (Right) The generated angle distribution compared to observed data.
</div>