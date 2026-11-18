---
layout: page
title: GNN4ITk and Exa.TrkX
description: Graph neural networks and GPU inference for particle track reconstruction.
img: assets/img/trackml_display.png
importance: 1
category: Machine Learning for High Energy Physics
---

Particle tracking reconstructs trajectories from detector hits. The number of possible hit combinations grows quickly in dense collision events. The Exa.TrkX project developed a graph-based approach that learns which hits belong together. I now develop ATLAS GNN4ITk and contribute to its ACORN research framework.

## Graph construction and track finding

- [**Double Metric Learning**](https://arxiv.org/abs/2605.14131) learns an asymmetric distance to connect successive detector hits. In simulated ATLAS ITk top-quark pair events at mean pileup 200, its undirected graphs averaged 6.59 million edges versus 6.97 million for Simple Metric Learning, with graph construction efficiencies of 99.72% and 99.81%, respectively.
- [**D-WALK and Junction Resolution**](https://indico.cern.ch/event/1471803/contributions/6967258/) address track segmentation. On ColliderML at mean pileup 200, D-WALK cut mean CPU segmentation time from 118 to 23 ms while retaining 98.6% track-finding efficiency. Junction Resolution improved track-finding efficiency from 95.1% to 98.3% versus Junction Removal, with mean CPU segmentation times of 16 and 15 ms, respectively.
- [**EggNet**](https://arxiv.org/abs/2407.13925) is an evolving graph attention network I proposed and developed. I presented it at the ICML 2024 AI for Science Workshop. The paper lists authors alphabetically by surname, independent of individual contributions. In the [CHEP performance study](https://doi.org/10.1051/epjconf/202533701121), segmented-graph training on TrackML used about one-tenth the training time and GPU memory of full-graph training.

## Tracking-as-a-Service

I serve GNN4ITk through NVIDIA Triton Inference Server with Athena as the client. My work evaluates latency with TensorRT, ONNX Runtime, and different numerical precisions, and measures throughput as client process and thread counts, model instances, and GPUs vary.

{% include figure.html path="assets/img/pipeline.png" alt="Stages of the Exa.TrkX track formation pipeline" class="img-fluid rounded" caption="The Exa.TrkX TrackML inference pipeline. Light red boxes mark trainable stages." %}
