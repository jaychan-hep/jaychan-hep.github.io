---
layout: page
title: HadML
description: Deep generative models for hadronization in particle event simulation.
img: assets/img/ENP_WEB.jpg
importance: 2
category: Machine Learning for High Energy Physics
---

Hadronization is the process by which quarks and gluons form the particles measured by detectors. I develop generative models that can be fitted to observed hadron distributions and evaluated against conventional event generators such as Herwig.

In [Fitting a deep generative hadronization model](https://doi.org/10.1007/JHEP09(2023)084), we fitted a generative adversarial network to two Herwig configurations using final-state hadrons as fit targets. An auxiliary neural classifier distinguished the configurations with an AUC of 0.77, compared with 0.57 for the best individual observable tested.

In [Integrating particle flavor into deep learning models for hadronization](https://doi.org/10.1103/hgbg-k7js), we extended HadML to generate both kinematics and particle identities for two-body cluster decays. The model reproduced Herwig’s shift toward strange hadrons when an incoming quark was strange.

{% include figure.html path="assets/img/MLHadv2.png" alt="Diagram of the HadML generative adversarial model" class="img-fluid rounded" bkg-white=true caption="Model architecture for fitting HadML to final-state hadron distributions." %}

[Training history (PDF)]({{ '/assets/img/loss_vs_epochs.pdf' | relative_url }}) · [Generated angle distribution (PDF)]({{ '/assets/img/theta_truthframe.pdf' | relative_url }})
