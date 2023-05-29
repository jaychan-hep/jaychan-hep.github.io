---
layout: page
title: Exa.TrkX
description: GNN-based pipeline for particle tracking
img: assets/img/trackml_display.png
importance: 1
category: Machine Learning for High Energy Physics
---

As particle accelerators become more powerful, detectors become more complex with increasingly dense measurements: O(10M) particles/second, O(100M) measurements/second. Traditional algorithms generate all possible trajectories, which result in a combinatorial explosion.

With the DOE Exa.TrkX project, we pioneer the application of Geometric Deep Learning methods, specifically graph neural networks, to capture and regularize relationships between measurements. The optimized pipeline runs end-to-end on the NVIDIA V100 GPU with a 20X speed-up wrto using a 48-core Xeon 8268s Cascade Lake CPU.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/ATLAS_reco_WtPerEvent_NOfit_revised.png" title="example image" class="img-fluid rounded z-depth-1" bkg-white=true zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/cpu_13nedges.pdf" title="example image" class="img-fluid rounded z-depth-1" bkg-white=true zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/gpu_8khits.pdf" title="example image" class="img-fluid rounded z-depth-1" bkg-white=true zoomable=true %}
    </div>
</div>
<div class="caption">
    (Left) Reconstruction wall time per event as a function of the average number of interactions per bunch crossing ⟨μ⟩ with the default configurations of ATLAS Run 2 Inner Detector reconstruction. (Middle) Total inference time with Exa.TrkX as a function of number of space-points in each event for CPUs. (Right) Exa.TrkX inference time for GPUs.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/pipeline.png" title="example image" class="img-fluid rounded z-depth-1" bkg-white=true zoomable=true %}
    </div>
</div>
<div class="caption">
    Stages of the TrackML track formation inference pipeline. Light red boxes are trainable stages.
</div>

